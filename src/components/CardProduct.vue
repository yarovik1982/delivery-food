<script setup>
const prpps = defineProps({
   item:{type:Object,required:true},
})
</script>
<template>
    <div class="col">
        <div class="card h-100" id="1">
          <img :src="item.productImage" class="card-img-top" :alt="item.productTitle">
          <div class="card-body">
            <h5 class="card-title">{{item.productTitle}}</h5>
            <p class="card-text">{{item.productDescription}}</p>
            <p class="card-text">{{item.productPrice}} ₽</p>

          </div>
          <div class="card-footer">
            <div class="d-flex align-items-center py-1 justify-content-between">
              <button class="btn btn-primary btn-sm" @click="handleClick(item)">В корзину</button>
            </div>
          </div>
        </div>
      </div>
</template>
<style scoped >

</style>