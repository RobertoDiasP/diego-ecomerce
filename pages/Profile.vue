<template>
  <section class="section">
    <div class="container">
      <h2 class="title">My Profile</h2>
      <div class="content">
        <p>
          <strong>Username:</strong>
          {{ loggedInUser.name }}
        </p>
        <p>
          <strong>Email:</strong>
          {{ loggedInUser.email }}
        </p>
      </div>
    </div>
  </section>
</template>

<script>
  import {
    mapGetters
  } from 'vuex'

  export default {
    middleware: 'auth',
    name: "profile-page",
    computed: {
      ...mapGetters(['loggedInUser'])
    }
  }

</script>
