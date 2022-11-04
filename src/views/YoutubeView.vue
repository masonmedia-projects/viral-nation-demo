<template>
   <div>
     <!-- subnav -->
      <nav class="navbar bg-light border-bottom">
         <div class="container-fluid">
            <div type="button" class="ms-auto me-2"
               data-bs-toggle="offcanvas" data-bs-target="#offcanvasWithBothOptions" aria-controls="offcanvasWithBothOptions">
               <svg xmlns="http://www.w3.org/2000/svg" width="26" height="26" fill="currentColor" class="bi bi-justify-left" viewBox="0 0 16 16">
                  <path fill-rule="evenodd" d="M2 12.5a.5.5 0 0 1 .5-.5h7a.5.5 0 0 1 0 1h-7a.5.5 0 0 1-.5-.5zm0-3a.5.5 0 0 1 .5-.5h11a.5.5 0 0 1 0 1h-11a.5.5 0 0 1-.5-.5zm0-3a.5.5 0 0 1 .5-.5h11a.5.5 0 0 1 0 1h-11a.5.5 0 0 1-.5-.5zm0-3a.5.5 0 0 1 .5-.5h11a.5.5 0 0 1 0 1h-11a.5.5 0 0 1-.5-.5z"/>
               </svg>
            </div>
            <div class="border border-left border-top-0 border-end-0 border-bottom-0 me-2" style="height: 23px"></div>
            <div type="button" class="me-3">
               <svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" fill="currentColor" class="bi bi-gear me-auto" viewBox="0 0 16 16">
                  <path d="M8 4.754a3.246 3.246 0 1 0 0 6.492 3.246 3.246 0 0 0 0-6.492zM5.754 8a2.246 2.246 0 1 1 4.492 0 2.246 2.246 0 0 1-4.492 0z"/>
                  <path d="M9.796 1.343c-.527-1.79-3.065-1.79-3.592 0l-.094.319a.873.873 0 0 1-1.255.52l-.292-.16c-1.64-.892-3.433.902-2.54 2.541l.159.292a.873.873 0 0 1-.52 1.255l-.319.094c-1.79.527-1.79 3.065 0 3.592l.319.094a.873.873 0 0 1 .52 1.255l-.16.292c-.892 1.64.901 3.434 2.541 2.54l.292-.159a.873.873 0 0 1 1.255.52l.094.319c.527 1.79 3.065 1.79 3.592 0l.094-.319a.873.873 0 0 1 1.255-.52l.292.16c1.64.893 3.434-.902 2.54-2.541l-.159-.292a.873.873 0 0 1 .52-1.255l.319-.094c1.79-.527 1.79-3.065 0-3.592l-.319-.094a.873.873 0 0 1-.52-1.255l.16-.292c.893-1.64-.902-3.433-2.541-2.54l-.292.159a.873.873 0 0 1-1.255-.52l-.094-.319zm-2.633.283c.246-.835 1.428-.835 1.674 0l.094.319a1.873 1.873 0 0 0 2.693 1.115l.291-.16c.764-.415 1.6.42 1.184 1.185l-.159.292a1.873 1.873 0 0 0 1.116 2.692l.318.094c.835.246.835 1.428 0 1.674l-.319.094a1.873 1.873 0 0 0-1.115 2.693l.16.291c.415.764-.42 1.6-1.185 1.184l-.291-.159a1.873 1.873 0 0 0-2.693 1.116l-.094.318c-.246.835-1.428.835-1.674 0l-.094-.319a1.873 1.873 0 0 0-2.692-1.115l-.292.16c-.764.415-1.6-.42-1.184-1.185l.159-.291A1.873 1.873 0 0 0 1.945 8.93l-.319-.094c-.835-.246-.835-1.428 0-1.674l.319-.094A1.873 1.873 0 0 0 3.06 4.377l-.16-.292c-.415-.764.42-1.6 1.185-1.184l.292.159a1.873 1.873 0 0 0 2.692-1.115l.094-.319z"/>
               </svg>
            </div>
         </div>
      </nav>
      <!-- offcanvas -->
      <div class="offcanvas offcanvas-end" data-bs-scroll="true" tabindex="-1" id="offcanvasWithBothOptions" aria-labelledby="offcanvasWithBothOptionsLabel">
         <div class="offcanvas-header bg-light border-bottom">
            <h5 class="offcanvas-title fw-bold" id="offcanvasWithBothOptionsLabel">creator</h5>
            <button type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Close"></button>
         </div>
         <div class="offcanvas-body">
            <ul class="list-unstyled">
                <router-link to="/instagram">
                    <li class="py-4 fs-5 fw-900 text-secondary border-bottom">
                        <img class="me-1" style="width: 25px" src="@/assets/img/instagram.svg" alt="">  Instagram
                    </li>
               </router-link>
               <router-link to="/facebook">
                <li class="py-4 fs-5 fw-900 text-secondary border-bottom">
                    <img class="me-1" style="width: 25px" src="@/assets/img/facebook.svg" alt=""> Facebook
                </li>
               </router-link>
               <router-link to="/youtube">
                <li class="py-4 fs-5 fw-900 text-secondary border-bottom">
                    <img class="me-1" style="width: 25px" src="@/assets/img/youtube.svg" alt=""> Youtube
                </li>
               </router-link>
               <li class="py-4 fs-5 fw-900 text-secondary border-bottom">
                  <img class="me-1" style="width: 25px" src="@/assets/img/tiktok.svg" alt=""> TikTok
               </li>
               <li class="py-4 fs-5 fw-900 text-secondary border-bottom">
                  <img class="me-1" style="width: 25px" src="@/assets/img/pinterest.svg" alt=""> Pinterest
               </li>
               <li class="py-4 fs-5 fw-900 text-secondary border-bottom">
                  <img class="me-1" style="width: 25px" src="@/assets/img/snapchat.svg" alt=""> Snapchat
               </li>
            </ul>
         </div>
      </div>

      <!-- hero -->
      <div class="container-fluid px-0">
        <div class="row m-0">
            <div class="col-lg-12 min-vh-50 left-center bg-light p-5">
                <h1 class="display-1 text-primary fw-900 ls-1">Explore {{ location.name }}.</h1>
                <h4 class="fw-bold text-secondary">Browse top trends, users, topics, and content.</h4>
            </div>
        </div>
      </div>

      <!-- main dashboard tab nav -->
      <nav class="nav nav-pills flex-column flex-sm-row border-bottom p-3">
         <button class="nav-link active flex-sm-fill text-sm-center border border-primary rounded-5 mx-2" id="home-tab" data-bs-toggle="tab" data-bs-target="#home-tab-pane" type="button" role="tab" aria-controls="home-tab-pane" aria-selected="true">Trending</button>
         <button @click="getData" class="nav-link flex-sm-fill text-sm-center border border-primary rounded-5 mx-2" id="contact-tab" data-bs-toggle="tab" data-bs-target="#contact-tab-pane" type="button" role="tab" aria-controls="contact-tab-pane" aria-selected="false">Users</button>
         <button @click="getPosts" class="nav-link flex-sm-fill text-sm-center border border-primary rounded-5 mx-2" id="disabled-tab" data-bs-toggle="tab" data-bs-target="#disabled-tab-pane" type="button" role="tab" aria-controls="disabled-tab-pane" aria-selected="false">Topics</button>
         <button class="nav-link flex-sm-fill text-sm-center border border-primary rounded-5 mx-2" id="profile-tab" data-bs-toggle="tab" data-bs-target="#profile-tab-pane" type="button" role="tab" aria-controls="profile-tab-pane" aria-selected="false">Search</button>
      </nav>
      <!-- tabs -->
      <div class="tab-content" id="myTabContent">
         <div class="tab-pane fade show active" id="home-tab-pane" role="tabpanel" aria-labelledby="home-tab" tabindex="0">
            <div class="container-fluid">
               <div class="row w-100 p-3 m-0 border-bottom" v-for="(item, index) in users.results" :key="index">
                  <div class="col-md-2 center-center p-2">
                     <img style="width: 150px" class="rounded-4 shadow" :src="item.picture.large" alt="...">
                  </div>
                  <div class="col-md-10 justify-content-center border border-start border-end-0 border-top-0 border-bottom-0 ps-4">
                     <h5>{{ item.name.first }} {{ item.name.last }}</h5>
                     <h6 class="text-secondary fw-light">@{{ item.login.username }}</h6>
                     <p>Deserunt nostrud id velit ea exercitation. Ullamco ullamco eu Lorem dolor minim eu exercitation esse ad. Est est do ea elit. Duis in amet reprehenderit reprehenderit anim.</p>
                     <button class="btn btn-outline-success btn-sm me-2">add</button>
                     <button class="btn btn-outline-danger btn-sm me-2">remove</button>
                     <button class="btn btn-outline-primary btn-sm">more</button>
                  </div>
               </div>
            </div>
         </div>
         <!-- search -->
         <div class="tab-pane fade" id="profile-tab-pane" role="tabpanel" aria-labelledby="profile-tab" tabindex="0">
            <div class="container-fluid px-0">
               <div class="row w-100 m-0 px-4 py-3">
                  <div class="col-lg-12 min-vh-50 bg-primary rounded-4 left-center p-5">
                     <h2 class="section-title text-light text-left fw-900">Search</h2>
                     <input type="email" class="form-control border-0 rounded-3" id="exampleFormControlInput1" placeholder="Search...">
                  </div>
               </div>
            </div>
         </div>
         <!-- users -->
         <div class="tab-pane fade" id="contact-tab-pane" role="tabpanel" aria-labelledby="contact-tab" tabindex="0">
            <div class="container-fluid">
               <div class="row w-100 p-3 m-0">
                  <div class="col-lg-3 col-md-4 col-sm-6 p-0" v-for="(item, index) in content.users" :key="index">
                     <div class="card m-3 p-3 rounded-4 bg-light">
                        <img :src="item.image" class="card-img-top w-25 mx-3 rounded-5 shadow" alt="...">
                        <div class="card-body">
                           <h6 class="text-secondary fw-light">@{{ item.username }}</h6>
                           <h5 class="card-title">{{ item.firstName + ' ' + item.lastName}}</h5>
                           <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
                           <a href="#" class="btn btn-outline-primary">Explore</a>
                        </div>
                     </div>
                  </div>
               </div>
            </div>
         </div>
         <!-- posts + images -->
         <div class="tab-pane fade" id="disabled-tab-pane" role="tabpanel" aria-labelledby="disabled-tab" tabindex="0">
            <div class="container-fluid">
               <div class="row w-100 p-3 m-0">
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
   import { useRoute } from "vue-router";
   const location = useRoute();
   const userData = ref([])
   const url = "https://randomuser.me/api/?results=100"

    const content = ref([]);
    const posts = ref([]);
    const users = ref([])
    const images = ref([])
   
     async function getData() {
       const res = await fetch("https://dummyjson.com/users");
       const finalRes = await res.json();
       content.value = finalRes;
       console.log(finalRes.users)
     }
     
     async function getUsers() {
       const res = await fetch(" https://randomuser.me/api/?results=30");
       const userData = await res.json();
       users.value = userData;
       console.log(userData.results)
     }
     
     async function getPosts() {
       const res = await fetch("https://dummyjson.com/posts");
       const postData = await res.json();
       posts.value = postData;
       console.log(postData.posts)
     }
   
     async function getImages() {
       const res = await fetch("https://picsum.photos/v2/list?page=2&limit=30");
       const imageData = await res.json();
       images.value = imageData;
       console.log(images)
     }
   
   //  getData()
    getUsers()
</script>