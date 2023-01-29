<template>
  <div class="card" style="width: 18rem">
    <img class="card-img-top" :src="user.info.pic" alt="Card image cap" />
    <div class="card-body">
      <h5 class="card-title">{{ user.info.name }}</h5>
      <p class="card-text">
        {{ user.info.description }}
      </p>
      <a href="#" class="btn btn-primary">Go somewhere</a>
    </div>
  </div>
</template>

<script setup>
  import {onMounted,reactive} from 'vue';
  const user = reactive({info:{}})

  async function getBio(){
    return await new Promise(resolve => {
      setTimeout(() => {
        resolve({
          pic: 'https://randomuser.me/api/portraits/men/5.jpg',
          name:'Joao Pedro',
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ex neque labore facilis saepe exercitationem ipsa vitae doloribus laborum quaerat accusamus magni blanditiis, iure nemo perferendis dolores, ea qui omnis hic!'
        })
      }, 1200)
    })
  }

  user.info = await getBio();
</script>