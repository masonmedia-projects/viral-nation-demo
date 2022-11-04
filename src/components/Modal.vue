<script setup>
const props = defineProps({
  modalId: { type: String },
  modalClose: {type: String },
  layout: {type: Number }
})
</script>

<template>
        <!-- Modal -->
<div class="modal fade" :id="modalId" data-bs-keyboard="false" tabindex="-1" aria-labelledby="staticBackdropLabel" aria-hidden="true">
  <div class="modal-dialog modal-dialog-centered">
    <div class="modal-content">
      <div class="modal-header">
        <h1 class="modal-title fs-5 fw-900" id="staticBackdropLabel">creator</h1>
        <button type="button" class="btn-close" :data-bs-dismiss="modalClose" aria-label="Close"></button>
      </div>
      <div class="modal-body px-5 pb-5 pt-4">
        <div v-if="layout === 1">
            <form>
                <div class="mb-3">
                <label for="exampleInputEmail1" class="form-label fw-900 text-secondary">Email</label>
                <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp">
                <!-- <div id="emailHelp" class="form-text">We'll never share your email with anyone else.</div> -->
                </div>
                <div class="mb-3">
                    <label for="exampleInputPassword1" class="form-label fw-900 text-secondary">Password</label>
                    <input type="password" class="form-control" id="exampleInputPassword1">
                </div>
                <button type="submit" class="btn btn-primary">Sign up</button>
            </form>
        </div>

        <div v-if="layout === 2">
            <form>
                <div class="mb-3">
                <label for="exampleInputEmail2" class="form-label">Email address</label>
                <input type="email" class="form-control" id="exampleInputEmail2" aria-describedby="emailHelp">
                <div id="emailHelp" class="form-text">We'll never share your email with anyone else.</div>
                </div>
                <div class="mb-3">
                    <label for="exampleInputPassword2" class="form-label">Password</label>
                    <input type="password" class="form-control" id="exampleInputPassword2">
                </div>
                <button type="submit" class="btn btn-primary">Login</button>
            </form>
        </div>
      </div>
      <!-- <div class="modal-footer">
        <button type="button" class="btn btn-secondary" :data-bs-dismiss="modalClose">Close</button>
        <button type="button" class="btn btn-primary">Login</button>
      </div> -->
    </div>
  </div>
</div>
</template>

<style lang="scss" scoped>

</style>