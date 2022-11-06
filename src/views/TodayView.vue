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
<!-- posts -->
<div class="row w-100 px-5 pb-5">
    <div class="col-lg-12">
                  <h3 class="fw-900 border-bottom pb-3">Posts</h3>
              </div>
          <div class="col-lg-4 col-md-6 p-0" v-for="(item, index) in posts.data" :key="index">
                     <div class="card m-3 p-3 rounded-4 bg-light">
                        <img v-if="index == 0" src="https://picsum.photos/1200/600?random=1" class="w-100 rounded-4" alt="">
                        <img v-if="index == 1" src="https://picsum.photos/1200/600?random=2" class="w-100 rounded-4" alt="">
                        <img v-if="index == 2" src="https://picsum.photos/1200/600?random=3" class="w-100 rounded-4" alt="">
                        
                        <div class="card-body">
                           <h5 class="text-secondary fw-light">@{{ item.author }}</h5>
                           <span class="badge text-bg-light border me-1 mb-3">{{ item.genre }}</span>
                           <h5 class="card-title">{{ item.title }}</h5>
                           <p class="card-text">{{ item.description }}</p>
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
// date
const date = new Date();
const months = ["January","February","March","April","May","June","July","August","September","October","November","December"];
const month = months[date.getMonth()];
const year = date.getFullYear();
const day = date.getDay();

const userData = ref([])
const url = "https://randomuser.me/api/?results=100"
 const content = ref([]);
 const posts = ref([]);
 const testData = ref([]);

  async function getData() {
    const res = await fetch("https://randomuser.me/api/?results=4");
    const finalRes = await res.json();
    content.value = finalRes;
    console.log(finalRes.results)
  }
  async function getPosts() {
    const res = await fetch("https://fakerapi.it/api/v1/books?_quantity=3");
    // const res = await fetch("https://dummyjson.com/posts?limit=3");
    const postData = await res.json();
    posts.value = postData;
    console.log(postData.data)
    }

// async function getPosts(){
//     const url1 = "https://fakerapi.it/api/v1/books?_quantity=3"
//     const url2 = "https://picsum.photos/v2/list?page=2&limit=3"
//     const responses = await Promise.all([fetch(url1), fetch(url2)])
//     let data1 = await responses[0].json()
//     let data2 = await responses[1].json()
//     posts.value = data1.data, data2;
//     console.log(data1, data2)
// }

// https://gomakethings.com/waiting-for-multiple-all-api-responses-to-complete-with-the-vanilla-js-promise.all-method/
//    function getPosts()  {
//        Promise.all([
// 	fetch('https://fakerapi.it/api/v1/books?_quantity=4'),
// 	fetch('https://jsonplaceholder.typicode.com/albums/2/photos')
// ]).then(function (responses) {
// 	return Promise.all(responses.map(function (response) {
// 		return response.json();
// 	}));
// }).then(function (data) {
//     posts.value = data;
// 	console.log(posts.value);
// }).catch(function (error) {
// 	console.log(error);
// });
// }

// https://hackmamba.io/blog/2020/12/aggregate-multiple-api-requests-with-promise-all/
// const fetchNames = async () => {
//       try {
//         const res = await Promise.all([
//           fetch("https://fakerapi.it/api/v1/books?_quantity=3"),
//           fetch("https://picsum.photos/v2/list?page=2&limit=3"),
//         //   fetch("./names-old.json")
//         ]);
//         const data = await Promise.all(res.map(r => r.json()))
//         textData.value = data;
//         console.log(textData.flat());
//       } catch {
//         throw Error("Promise failed");
//       }
// };

// fetchNames()

// function test() {
//     Promise.all([
//   fetch('https://fakerapi.it/api/v1/books?_quantity=3').then(resp => resp.json()),
//   fetch('https://jsonplaceholder.typicode.com/albums/2/photos').then(resp => resp.json()),
// //   fetch('https://jsonplaceholder.typicode.com/posts/3').then(resp => resp.json()),
// ]).then((data) => {
//     testData.value = data;
//     console.log(testData)
// })
// }

// test();

 getData();
 getPosts();
</script>
