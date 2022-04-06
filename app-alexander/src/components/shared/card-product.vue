<template>
    <div class="content">
        <li v-for="p in products" :key="p.id">
            <div class="card">
                <div class="imgBox">
                    <img :src=p.urlImage :alt=p.name  width="100px" height="10px" />
                </div>
            <div>
            <div class="contentBox">
                <h3>{{p.name}}</h3>
                <h2 class="price">$ {{p.price}} </h2>
            </div>
            </div>
            </div>
        </li>
    </div>
</template>

<script>
import axios from "axios";

function mounted() {
  const urlAPI = "https://ec-products.makipos.la/v2/";
  axios
    .get(urlAPI + "products?flagActive=1&page=1&warehouses=1931&limit=20 ", {
      headers: {
        Authorization: `Bearer ${localStorage.getItem("token")}`,
      },
    })
    .then((response) => {
        console.log(response);
      const { data } = response;
      this.products = data
    })
    .catch(function (error) {
      console.log(error);
    });
}

function data() {
  return {
    products: [],
  };
}

export default {
  name: "card-product",
  mounted,
  data,
};
</script>

<style scoped>

    li {
        list-style: none;
    }

    .card {
        float: left;
        position: relative;
        margin: 10px;
        width: 320px;
        height: 300px;
        background: #339e95;
        border-radius: 20px;
        overflow: hidden;
    }

    .card .imgBox{
        position: relative;
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        padding-top:20px;
        z-index: 1;
    }

    @media screen and (max-width: 600px) {
    .card {
        width: 100%;
        display: block;
        margin-bottom: 20px;
    }
}

</style>