<script setup>
import CardProduct from '@/components/CardProduct.vue'
const products = [
   {id:1,productTitle:'Ролл угорь стандарт',productDescription:'Рис, угорь, соус унаги, кунжут, водоросли нори.',productPrice:250,productImage:"src/assets/images/product-1.jpg"},
   {id:2,productTitle:'Калифорния лосось стандарт',productDescription:'Рис, лосось, авокадо, огурец, майонез, икра масаго, водоросли нори.',productPrice:395,productImage:"src/assets/images/product-2.jpg"},
   {id:3,productTitle:'Окинава стандарт',productDescription:' Рис, креветка отварная, сыр сливочный, лосось, огурец свежий...',productPrice:250,productImage:"src/assets/images/product-3.jpg"},
   {id:4,productTitle:'Цезарь маки хl',productDescription:'Рис, куриная грудка копченая, икра масаго, томат, айсберг, соус цезарь...',productPrice:250,productImage:"src/assets/images/product-4.jpg"},
   {id:5,productTitle:'Ясай маки стандарт 185 г',productDescription:'Рис, помидор свежий, перец болгарский, авокадо, огурец, айсберг',productPrice:250,productImage:"src/assets/images/product-5.jpg"},
   {id:6,productTitle:'Ролл с креветкой стандарт',productDescription:'Рис, водоросли нори, креветки отварные, сыр сливочный, огурцы',productPrice:250,productImage:"src/assets/images/product-6.jpg"},
]
</script>
<template>
   <div class="layout " id="layout">
    <div class="layout-content bg-body-tertiary ">
      <div class="table-responsive">
        <table class="table text-center table-bordered align-middle">
          <thead>
            <tr>
              <th scope="col">№ поз.</th>
              <th scope="col">Наименование</th>
              <th scope="col">Количество</th>
              <th scope="col">Цена за единицу</th>
              <th scope="col">Сумма</th>
              <th scope="col">Действия</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <th scope="row">1</th>
              <td class="title"></td>
              <td class="quantity"></td>
              <td class="price"></td>
              <td class="sum"></td>
              <td class="d-flex">
                <i class="bi bi-plus-square-dotted fs-2" onclick="increment(this)"></i>
                <i class="bi bi-dash-square-dotted fs-2 ms-3 me-3" onclick="decrement(this)"></i>
                <i class="bi bi-trash3 fs-2" onclick="delete(this)"></i>
              </td>
            </tr>
            <tr>
              <th scope="row">2</th>
              <td>Jacob</td>
              <td>Thornton</td>
              <td>@fat</td>
              <td>@fat</td>
              <td>@fat</td>
            </tr>
            <tr>
              <th scope="row">3</th>
              <td>Larry the Bird</td>
              <td>Larry the Bird</td>
              <td>@twitter</td>
              <td>@twitter</td>
              <td>@twitter</td>
            </tr>
          </tbody>
          <tfoot>
            <th scope="row" colspan="4">Итого</th>
            <th colspan="2">1000</th>

          </tfoot>
        </table>
      </div>
    </div>
  </div>


  <h1 class="text-center bg-body-tertiary m-0" id="title">
    Kazan-Mangal
  </h1>
  <nav class="navbar navbar-dark bg-body-tertiary" style="position:sticky; top:0; z-index: 10;"
    aria-label="Пример первой панели навигации">
    <div class="container-fluid">

      <button class="navbar-toggler collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#navbar"
        aria-controls="navbar" aria-expanded="false" aria-label="Переключить навигацию">
        <span class="navbar-toggler-icon"></span>
      </button>

      <i class="bi bi-cart2 fs-1" id="cart" data-count="0"></i>

      <div class="navbar-collapse collapse" id="navbar">
        <ul class="navbar-nav me-auto mb-2">
          <li class="nav-item">
            <a class="nav-link active" aria-current="page" href="#">Главная</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Ссылка</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Отключенная</a>
          </li>
        </ul>

      </div>
    </div>
  </nav>

  <div class="container">
    <div class="row row-cols-1 row-cols-md-3 g-4 py-5" id="products">
      <CardProduct
         :item="item" 
         v-for="item in products"
         :key="item.id"
      ></CardProduct>
   </div>
  </div>
</template>
<style scoped >

</style>