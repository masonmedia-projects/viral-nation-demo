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
            <div class="col-lg-12 min-vh-75 center-center p-5">
                <h1 class="display-1 lh-1 mb-3 text-primary fw-900 ls-1">Explore. Engage. Create.</h1>
                <h4 class="fw-bold text-secondary mb-3">Browse top trends, users, topics, and content.</h4>
              <div class="d-flex ">
                <router-link to="/instagram">
                  <button class="btn btn-link me-3">
                    <img style="width: 60px" src="@/assets/img/instagram.svg" alt="">
                  </button>
                </router-link>
                <router-link to="/facebook">
                  <button class="btn btn-link me-3">
                    <img style="width: 60px" src="@/assets/img/facebook.svg" alt="">
                  </button>
                </router-link>
                <router-link to="/youtube">
                  <button class="btn btn-link me-3">
                    <img style="width: 60px" src="@/assets/img/youtube.svg" alt="">
                  </button>
                </router-link>
                <router-link to="/">
                  <button class="btn btn-link me-3">
                    <img style="width: 60px" src="@/assets/img/tiktok.svg" alt="">
                  </button>
                </router-link>
                <router-link to="/">
                  <button class="btn btn-link me-3">
                    <img style="width: 60px" src="@/assets/img/pinterest.svg" alt="">
                  </button>
                </router-link>
                <router-link to="/">
                  <button class="btn btn-link me-3">
                    <img style="width: 60px" src="@/assets/img/snapchat.svg" alt="">
                  </button>
                </router-link>
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