<template>
    <nav class="navbar navbar-expand-lg bg-light border-bottom">
            <div class="container-fluid">
                <router-link class="navbar-brand fw-bold bw-900" to="/">creator</router-link>
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
                <div class="navbar-nav ms-auto">
                    <router-link class="nav-link" to="/mycreator">Home</router-link>
                    <router-link class="nav-link" to="/about">About</router-link>
                    <router-link class="nav-link" to="/create">Create</router-link>
                    <router-link class="nav-link" to="/blog">Blog</router-link>
                    <div class="border border-left border-top-0 border-end-0 border-bottom-0 mx-1"></div>
                    <div class="ms-3">
                        <button class="btn btn-outline-primary me-2">Sign in</button>
                        <button class="btn btn-primary">Sign up</button>
                    </div>
                    <!-- sidenav -->
                    <!-- Button trigger modal -->
                    <div class="border border-left border-top-0 border-end-0 border-bottom-0 ms-3"></div>

                    <button type="button" class="btn btn-link" data-bs-toggle="modal" data-bs-target="#exampleModal">
                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-three-dots-vertical" viewBox="0 0 16 16">
                    <path d="M9.5 13a1.5 1.5 0 1 1-3 0 1.5 1.5 0 0 1 3 0zm0-5a1.5 1.5 0 1 1-3 0 1.5 1.5 0 0 1 3 0zm0-5a1.5 1.5 0 1 1-3 0 1.5 1.5 0 0 1 3 0z"/>
                    </svg>
                    </button>

                    <!-- Modal -->
                    <div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
                    <div class="modal-dialog modal-fullscreen modal-dialog-scrollable">
                        <div class="modal-content">
                        <div class="modal-header">
                            <h1 class="modal-title fw-900 fs-2" id="exampleModalLabel">creator</h1>
                            <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                        </div>
                        <div class="modal-body d-flex flex-column align-items-start justify-content-end">
                            <router-link class="nav-link fs-5 fw-900 lh-1" to="/">Search</router-link>
                            <router-link class="nav-link fs-5 fw-900 lh-1" to="/about">Today</router-link>
                            <router-link class="nav-link fs-5 fw-900 lh-1" to="/create">Users</router-link>
                            <router-link class="nav-link fs-5 fw-900 lh-1" to="/blog">Trends</router-link>
                            <hr class="text-secondary w-100">                            
                            <router-link class="nav-link fs-5 fw-900 lh-1" to="/">Home</router-link>
                            <router-link class="nav-link fs-5 fw-900 lh-1" to="/">About</router-link>
                            <router-link class="nav-link fs-5 fw-900 lh-1" to="/">Blog</router-link>
                            
                            <hr class="text-secondary w-100">                            
                            <router-link class="nav-link fs-5 fw-900 lh-1" to="/">Settings</router-link>
                            <router-link class="nav-link fs-5 fw-900 lh-1" to="/">Logout</router-link>
                        </div>
                        <div class="modal-footer">
                            <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
                        </div>
                        </div>
                    </div>
                    </div>
                    
                </div>
                </div>
            </div>
        </nav>
</template>

<script setup>

</script>

<style scoped>

</style>