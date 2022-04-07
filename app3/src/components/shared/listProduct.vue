<template>
  <div>
      <h1>Productos en Venta</h1>
      <div class="row">
          <div class="col" v-for="product of products" :key="product.id">
              <div class="card">
                  <div class="img">
                      <img :src="product.urlImage" alt="">
                  </div>
                  <div class="character">
                        <h4>{{product.name}}</h4>
                        <span>$ {{product.cost}}</span>
                        <label>Descripcion:</label>
                        <span>{{product.description}}</span>
                  </div>
              </div>
          </div>
      </div>
  </div>
</template>

<script>
import axios from 'axios';

function mounted(){
    const token = localStorage.getItem('token');
    //console.log(token);
    axios.get('https://ec-products.makipos.la/v2/products?flagActive=1&page=1&warehouses=1931&limit=20',
    {
        headers:{
            'Authorization': 'Bearer ' + token
        }  
    }).then((response)=>{
        this.products = response.data
        console.log(this.products)
    })
}

function data(){
    return {
        products: []
    }
}

export default {
    name: 'listProduct',
    mounted,
    data,
}
</script>

<style scope>

    .img{
        width:5rem;
        height: auto;
        padding: 1rem;
    }

    img{
        width: 100%;
        height: auto;
        max-width: 10rem;
        border-radius: 20px;
    }

    .row{
        display: grid;
        grid-template-columns: repeat(3,1fr);
        grid-template-rows: repeat(7,1fr);
        background-color: #424242;
    }

    .col{
       border: 1px solid black; 
    }
    
    .card{
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .character{
        display: flex;
        flex-direction: column;
        color: #fff;
    }
</style>