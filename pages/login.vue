<template>
      <div class="container">
        <div class="row justify-content-center">
          <div class="col-md-6">
            <div class="card mt-5">
              <div class="card-header">
                <h3 class="card-title">Welcome Back</h3>
              </div>
                <div class="card-body">
                    <div class="mb-3">
                    <label for="email" class="form-label">Email address</label>
                    <input
                        type="email"
                        class="form-control"
                        id="email"
                        v-model="email"
                        required
                    />
        
                    </div>
                    <div class="mb-3">
                    <label for="password" class="form-label">Password</label>
                    <input
                        type="password"
                        class="form-control"
                        id="password"
                        v-model="password"
                        required
                    />
        
                    </div>
                    <button @click="handleSubmit" class="btn btn-primary" type="submit">
                    Sign-In
                    </button>
                </div>
            </div>
          </div>
        </div>
      </div>
    </template>
    
    <script setup>
    useHead({
      title: 'Login',
      link: [
        {
          href: 'https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/css/bootstrap.min.css',
          rel: 'stylesheet',
          integrity:
            'sha384-gH2yIJqKdNHPEq0n4Mqa/HGKIhSkIHeL5AyhkYV8i59U5AR6csBvApHHNl/vI1Bx',
          crossorigin: 'anonymous',
        },
      ],
      script: [
        {
          src: 'https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/js/bootstrap.bundle.min.js',
          integrity:
            'sha384-A3rJD856KowSb7dwlZdYEkO39Gagi7vIsF0jrRAoQmDKKtQBHUuLZ9AsSv4jD4Xa',
          crossorigin: 'anonymous',
        },
      ],
    });
    </script>
  
    <script>
    import Cookies from 'js-cookie'
    export default {
      data() {
        return {
          email: '',
          password: '',
        };
      },
      
      methods: {
       async handleSubmit() {
          // Handle login logic here
          
          console.log('Email:', this.email, 'Password:', this.password);
          try {
                  const url = 'http://localhost:5000/api/auth/login';
                  const response = await fetch(url , {
                      method: 'POST',
                      headers: {
                          'Content-Type': 'application/json',
                      },
                      body: JSON.stringify({
                          email: this.email,
                          password: this.password,
                      }),
                  });
                  const data = await response.json();
                  if (response.ok) {
                      console.log('Login successful:', data);
                      //Save response to cookies
                      Cookies.set('auth_token', 'your auth-token');
                      this.email = '';
                      this.password = '';
                      // Redirect to the dashboard
                      this.$router.push('/index1');
                      
                  } else {
                      console.error('Login failed:', data);
                  }
              } catch (error) {
                  console.error('Login failed:', error.message);
              }
        },
      },
    };
    </script>