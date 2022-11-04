<template>
    <div>
  <div class="container-fluid px-0">
      <div class="row m-0">
          <div class="col-lg-12 min-vh-50 left-center bg-light p-5">
              <h1 class="display-1 text-primary fw-900 ls-1">Get inspired.</h1>
              <h4 class="fw-bold text-secondary">Browse your daily curated trends</h4>
          </div>
      </div>
  </div>

<div class="tab-content" id="myTabContent">
  <div class="tab-pane fade show active" id="home-tab-pane" role="tabpanel" aria-labelledby="home-tab" tabindex="0">
      <div class="container-fluid px-0">
          <div class="row w-100 p-5">
              <div class="col-lg-12">
                  <h3 class="fw-900">{{ month + ' ' + day + ', ' + year }}</h3>
              </div>
              <div class="col-lg-3 col-md-4 col-sm-6 p-0" v-for="(item, index) in content.results" :key="index">
                  <div class="card m-3 p-3 rounded-4 bg-light">
                    <img :src="item.picture.large" class="card-img-top w-25 mx-3 rounded-5 shadow" alt="...">
                    <div class="card-body">
                        <h6 class="text-secondary fw-light">@{{ item.login.username }}</h6>
                        <h5 class="card-title">{{ item.name.first + ' ' + item.name.last}}</h5>
                        <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
                        <a href="#" class="btn btn-outline-primary">Explore</a>
                    </div>
                </div>
              </div>
          </div>
      </div>

  </div>
  <div class="tab-pane fade" id="profile-tab-pane" role="tabpanel" aria-labelledby="profile-tab" tabindex="0">...</div>
  <div class="tab-pane fade" id="contact-tab-pane" role="tabpanel" aria-labelledby="contact-tab" tabindex="0">...</div>
  <div class="tab-pane fade" id="disabled-tab-pane" role="tabpanel" aria-labelledby="disabled-tab" tabindex="0">...</div>
</div>

    </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'
const date = new Date();
const months = ["January","February","March","April","May","June","July","August","September","October","November","December"];
const month = months[date.getMonth()];
const year = date.getFullYear();
const day = date.getDay();

const userData = ref([])
const url = "https://randomuser.me/api/?results=100"

//   async function getData() {
//     const res = await fetch(url);
//     if(res.length !== 0) {
//         const finalRes = await res.json();
//         console.log(userData)
//     }
    
//   }

//  getData()
 const content = ref([]);

  async function getData() {
    const res = await fetch("https://randomuser.me/api/?results=4");
    const finalRes = await res.json();
    content.value = finalRes;
    console.log(finalRes.results)
  }

 getData()
</script>
