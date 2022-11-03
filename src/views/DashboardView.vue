<template>
    <div>
        <nav class="nav nav-pills flex-column flex-sm-row p-3">
            <button class="nav-link active flex-sm-fill text-sm-center border border-primary mx-2" id="home-tab" data-bs-toggle="tab" data-bs-target="#home-tab-pane" type="button" role="tab" aria-controls="home-tab-pane" aria-selected="true">Search</button>
            <button class="nav-link flex-sm-fill text-sm-center border border-primary mx-2" id="profile-tab" data-bs-toggle="tab" data-bs-target="#profile-tab-pane" type="button" role="tab" aria-controls="profile-tab-pane" aria-selected="false">Trending</button>
            <button @click="getData" class="nav-link flex-sm-fill text-sm-center border border-primary mx-2" id="contact-tab" data-bs-toggle="tab" data-bs-target="#contact-tab-pane" type="button" role="tab" aria-controls="contact-tab-pane" aria-selected="false">Users</button>
            <button @click="getPosts" class="nav-link flex-sm-fill text-sm-center border border-primary mx-2" id="disabled-tab" data-bs-toggle="tab" data-bs-target="#disabled-tab-pane" type="button" role="tab" aria-controls="disabled-tab-pane" aria-selected="false">Topics</button>
        </nav>

<div class="tab-content" id="myTabContent">
  <div class="tab-pane fade show active" id="home-tab-pane" role="tabpanel" aria-labelledby="home-tab" tabindex="0">
      <div class="container-fluid">
          <div class="row w-100 p-3">
              <div class="col-lg-3 col-md-4 col-sm-6 p-0" v-for="(item, index) in content.users" :key="index">
                  <div class="card m-3 p-3 rounded-4 bg-light">
                    <img :src="item.image" class="card-img-top w-25 mx-3 rounded-5 shadow" alt="...">
                    <div class="card-body">
                        <h6 class="text-secondary fw-light">@{{ item.username }}</h6>
                        <h5 class="card-title">{{ item.firstName + ' ' + item.lastName}}</h5>
                        <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
                        <a href="#" class="btn btn-primary">Add</a>
                    </div>
                </div>
              </div>
          </div>
      </div>
  </div>
  <!-- posts -->
  <div class="tab-pane fade" id="profile-tab-pane" role="tabpanel" aria-labelledby="profile-tab" tabindex="0">...</div>
  <div class="tab-pane fade" id="contact-tab-pane" role="tabpanel" aria-labelledby="contact-tab" tabindex="0">
<div class="container-fluid">
          <div class="row w-100 p-3">
              <div class="col-lg-3 col-md-4 col-sm-6 p-0" v-for="(item, index) in content.users" :key="index">
                  <div class="card m-3 p-3 rounded-4 bg-light">
                    <img :src="item.image" class="card-img-top w-25 mx-3 rounded-5 shadow" alt="...">
                    <div class="card-body">
                        <h6 class="text-secondary fw-light">@{{ item.username }}</h6>
                        <h5 class="card-title">{{ item.firstName + ' ' + item.lastName}}</h5>
                        <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
                        <a href="#" class="btn btn-primary">Add</a>
                    </div>
                </div>
              </div>
          </div>
      </div>
  </div>
  <!-- posts -->
  <div class="tab-pane fade" id="disabled-tab-pane" role="tabpanel" aria-labelledby="disabled-tab" tabindex="0">
      <div class="container-fluid">
          <div class="row w-100 p-3">
              <div class="col-lg-3 col-md-4 col-sm-6 p-0" v-for="(item, index) in posts.posts" :key="index">
                  <div class="card m-3 p-3 rounded-4 bg-light">
                    <img :src="item.image" class="card-img-top w-25 mx-3 rounded-5 shadow" alt="...">
                    <div class="card-body">
                        <h6 class="text-secondary fw-light">@{{ item.userId }}</h6>
                        <h5 class="card-title">{{ item.title }}</h5>
                        <p class="card-text">{{ item.body.slice(0, 150) }}</p>
                        <a href="#" class="btn btn-primary">View</a>
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
 const posts = ref([]);

  async function getData() {
    const res = await fetch("https://dummyjson.com/users");
    const finalRes = await res.json();
    content.value = finalRes;
    console.log(finalRes.users)
  }
  
  async function getPosts() {
    const res = await fetch("https://dummyjson.com/posts");
    const postData = await res.json();
    posts.value = postData;
    console.log(postData.posts)
  }

 getData()
</script>