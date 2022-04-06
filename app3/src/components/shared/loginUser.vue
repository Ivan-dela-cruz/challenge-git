<template>
<div class="containerr">
  <div class="container-form">
      <div class="text-center">
          <h1>Login</h1>
      </div>
      <form action="" class="form">
            <div class="form-group">
                <label for="" class="text-center">Username</label>
                <input type="text" class="form-control">
            </div>
            
            <div class="form-group">
                <label for="">Password</label>
                <input type="password" class="form-control">
            </div>
            <div>
                <button class="btn">Submit</button>
            </div>
      </form>
      
  </div>
</div>
</template>

<script>
export default {
    name: 'userLogin'
}
</script>

<style scope>

    .containerr{
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        background-color: #bdbdbd;
    }
    .container-form{
        width: 50%;
        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        background-color: #bdbdbd;
    }

    .form{
        display: flex;
        flex-direction: column;
        width: 20rem;
        height: 15rem;
        justify-content: center;
    }

    .text-center{
        text-align: center;
    }

    .form-group{
        display: flex;
        flex-direction: column;
    }

    .form-control{
        padding: 0.5rem;
        border-radius: 30px;
        margin: 10px;
    }

    .btn{
        border-radius: 30px;
        width: 10rem;
        height: 2.5rem;
    }
    .d-flex{
        display: flex;
    }

    .justify-content-center{
        justify-content: center;
    }
</style>