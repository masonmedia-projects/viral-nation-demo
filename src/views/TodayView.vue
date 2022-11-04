<template>
    <div>
  <div class="container-fluid px-0">
      <div class="row m-0">
          <div class="col-lg-12 min-vh-50 left-center bg-light p-5">
              <h1 class="display-1 text-primary fw-900 ls-1">Get inspired.</h1>
              <h4 class="fw-bold text-secondary">Browse your daily curated trends</h4>
              <h3 class="fw-900">{{ month + ' ' + day + ', ' + year }}</h3>
          </div>
      </div>
  </div>

<div class="tab-content" id="myTabContent">
  <div class="tab-pane fade show active" id="home-tab-pane" role="tabpanel" aria-labelledby="home-tab" tabindex="0">
      <div class="container-fluid px-0">
          <div class="row w-100 p-5">
              <div class="col-lg-12">
                  <h3 class="fw-900 border-bottom pb-3">Users</h3>
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

          <div class="row w-100 px-5 pb-5">
              <div class="col-lg-12">
                  <h3 class="fw-900 border-bottom pb-3">Video</h3>
              </div>
              <div class="col-lg-4 col-md-4 col-sm-6 p-0">
                  <div class="card m-3 p-3 rounded-4 bg-light">
                    <iframe width="100%" height="auto" src="https://www.youtube.com/embed/131OX_YHkwo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                    <div class="card-body px-0 pb-2">
                        <a href="#" class="btn btn-outline-primary btn-sm">Explore</a>
                    </div>
                </div>
              </div>
              <div class="col-lg-4 col-md-4 col-sm-6 p-0">
                  <div class="card m-3 p-3 rounded-4 bg-light">
                    <iframe width="100%" height="auto" src="https://www.youtube.com/embed/Jj7nurUPMnY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                    <div class="card-body px-0 pb-2">
                        <a href="#" class="btn btn-outline-primary btn-sm">Explore</a>
                    </div>
                </div>
              </div>
              <div class="col-lg-4 col-md-4 col-sm-6 p-0">
                  <div class="card m-3 p-3 rounded-4 bg-light">
                    <iframe width="100%" height="auto" src="https://www.youtube.com/embed/0arou9boK8k" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                    <div class="card-body px-0 pb-2">
                        <a href="#" class="btn btn-outline-primary btn-sm">Explore</a>
                    </div>
                </div>
              </div>
          </div>

<div class="row w-100 px-5 pb-5">
    <div class="col-lg-12">
                  <h3 class="fw-900 border-bottom pb-3">Posts</h3>
              </div>
          <div class="col-lg-4 col-md-6 p-0" v-for="(item, index) in posts.posts" :key="index">
                     <div class="card m-3 p-3 rounded-4 bg-light">
                        <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" fill="currentColor" class="bi bi-person-circle mx-3 text-secondary" viewBox="0 0 16 16">
                           <path d="M11 6a3 3 0 1 1-6 0 3 3 0 0 1 6 0z"/>
                           <path fill-rule="evenodd" d="M0 8a8 8 0 1 1 16 0A8 8 0 0 1 0 8zm8-7a7 7 0 0 0-5.468 11.37C3.242 11.226 4.805 10 8 10s4.757 1.225 5.468 2.37A7 7 0 0 0 8 1z"/>
                        </svg>
                        <div class="card-body">
                           <h5 class="text-secondary fw-light">@{{ item.userId }}</h5>
                           <span v-for="(i, index) in item.tags" :key="index" class="badge text-bg-light border me-1 mb-3">{{ i }}</span>
                           <h5 class="card-title">{{ item.title }}</h5>
                           <p class="card-text">{{ item.body.slice(0, 150) }}</p>
                           <a href="#" class="btn btn-sm  btn-secondary">Read more</a>
                        </div>
                     </div>
                  </div>
</div>

      </div>
  </div>
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

//  getData()
 const content = ref([]);
 const posts = ref([])

  async function getData() {
    const res = await fetch("https://randomuser.me/api/?results=4");
    const finalRes = await res.json();
    content.value = finalRes;
    console.log(finalRes.results)
  }
  async function getPosts() {
    const res = await fetch("https://dummyjson.com/posts?limit=3");
    const postData = await res.json();
    posts.value = postData;
    console.log(postData.posts)
    }

 getData();
 getPosts();
</script>
