<script setup>
import Modal from '../components/Modal.vue'
</script>

<template>
  <main>
    <div class="container-fluid px-0">
      <div class="row m-3 bg-primary rounded-5" style="min-height: 85vh">
        <div class="center-center" style="border-radius: 33px;">
        <div class="col-lg-12 center-center p-5">
          <h1 class="site-title fw-900">creator</h1>
          <p class="h5 col-md-6 col-offset-md-3 my-4 text-light">Increase content visibility, expand social media influence, and garner insights into top trends and best practices for content creation.</p>
          <div class="d-flex mx-auto">
            <button class="btn btn-outline-light me-2" data-bs-toggle="modal" data-bs-target="#staticBackdrop">Sign up</button>
            <router-link to="/mycreator">
            <button class="btn btn-outline-light">Get started</button>
            </router-link>
            <!-- <button class="btn btn-outline-light"
            data-bs-toggle="login" data-bs-target="#loginModal">Get started</button> -->
          </div>
        </div>
        </div>
        <Modal modalId="staticBackdrop" modalClose="modal" :layout="1"  />
        <Modal modalId="loginModal" modalClose="login"  />

<!-- Modal -->
<!-- <div class="modal fade" id="staticBackdrop" data-bs-keyboard="false" tabindex="-1" aria-labelledby="staticBackdropLabel" aria-hidden="true">
  <div class="modal-dialog modal-dialog-centered modal-lg">
    <div class="modal-content">
      <div class="modal-header">
        <h1 class="modal-title fs-5" id="staticBackdropLabel">Modal title</h1>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body">
        ...
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
        <button type="button" class="btn btn-primary">Understood</button>
      </div>
    </div>
  </div>
</div> -->

      </div>
    </div>
  </main>
</template>
