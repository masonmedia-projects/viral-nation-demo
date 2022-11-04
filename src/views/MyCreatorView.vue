<template>
    <div>
        <div class="container-fluid p-0">
            <div class="row m-3 text-light">
                <div class="col-md-6 p-0">
                    <router-link to="/today">
                    <div class="m-2 min-vh-50 rounded-xl center-center" style="background: #00A6ED">
                        <h2 class="fs-1 fw-900">Today</h2>
                    </div>
                    </router-link>
                </div>
                <div class="col-md-6 p-0">
                    <router-link to="/dashboard">
                    <div class="m-2 min-vh-50 rounded-xl center-center" style="background: #662E9B">
                        <h2 class="fs-1 fw-900">Trends</h2>
                    </div>
                    </router-link>
                </div>
                <div class="col-md-6 p-0">
                    <div class="m-2 min-vh-50 rounded-xl center-center" style="background: #F86624">
                        <h2 class="fs-1 fw-900">Learn</h2>
                    </div>
                </div>
                <div class="col-md-6 p-0">
                    <div class="m-2 min-vh-50 rounded-xl center-center" style="background: #F9C80E">
                        <h2 class="fs-1 fw-900">Archive</h2>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>

</script>

<style scoped>
a, a:hover {
    color: #ffffff;
    text-decoration: none;
}

</style>