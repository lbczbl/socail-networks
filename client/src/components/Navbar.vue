<template>
    <nav class="navbar navbar-expand-sm navbar-dark bg-dark mb-4">
        <div class="container">
            <router-link to="/" class="navbar-brand">创灵在线</router-link>
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#mobile-nav">
                <span class="navbar-toggler-icon"></span>
            </button>

            <div class="collapse navbar-collapse" id="mobile-nav">
                <ul class="navbar-nav mr-auto">
                    <li class="nav-item">
                        <router-link to="/profiles" class="nav-link">开发者</router-link>
                    </li>
                </ul>

                <ul class="navbar-nav ml-auto">
                    <li class="nav-item">
                        <router-link to="/register" class="nav-link">注册</router-link>
                    </li>
                    <li class="nav-item">
                        <router-link to="/login" class="nav-link">登录</router-link>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>

<script>
export default {
  name:'Navbar',
  data(){
      return {};
  }
}
</script>

<style scoped>

</style>

