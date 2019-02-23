<template>
    <div class="register">
        <div class="container">
            <div class="row">
                <div class="col-md-8 m-auto">
                    <h1 class="display-4 text-center">注册</h1>
                    <p class="lead text-center">创建新的账户</p>
                    <form @submit.prevent="submit" autocomplete="off">
                        <div class="form-group">
                            <input 
                                type="text" 
                                class="from-control form-control-lg" 
                                placeholder="用户名" 
                                name="name"
                                v-model="newUser.name"
                            />
                        </div>
                        <div class="form-group">
                            <input 
                                type="email" 
                                class="form-control from-control-lg" 
                                placeholder="邮箱地址" 
                                name="email"
                                v-model="newUser.email"
                            />
                            <small className="form-text text-muted">我们使用了gravatar全球公认头像，如果需要有头像显示，请使用在gravatar注册的邮箱</small>
                        </div>
                        <div class="form-group">
                            <input 
                                type="password" 
                                class="form-control form-control-lg" 
                                placeholder="密码" 
                                name="password"
                                v-model="newUser.password"
                            />
                            <TextField 
                                type='password'
                                name='password2'
                                placeholder="确认密码"
                                v-model="newUser.password2"
                                :error='errors.password2'
                            ></TextField>
                            <input type="submit"  class="btn btn-info btn-block mt-4" />
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Register',
  data() {
      return {
          newUser: {
              name:'',
              email:'',
              password:'',
              password2:'',
          },
          errors: ''
      };
  },
  methods: {
      submit() {
          console.log(this.newUser.name);
      }
  },
}

</script>

<style scoped>

</style>

