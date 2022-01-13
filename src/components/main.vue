<template>
  <div>
      <div class="content">
          <button class="push" @click="push">Push</button>
          <button class="button" @click="delate">Delate</button>
          <div class="box" v-for="id in boxItem" :key="id.title" v-on:click="id.show = !id.show">
              <p class="title"> {{ id.title }} </p>
              <p v-show="id.show" class="name"> {{ id.name }} </p>
          </div>
      </div>
  </div>
</template>

<script>
export default {
    data() {
        return {
            boxItem: [
                {title: 'name', name: 'Mirafzal',show: false},
                {title: 'name', name: 'Otabek',show: false},
                {title: 'name', name: 'Abdulaziz',show: false},
                {title: 'name', name: 'Azamat',show: false},
                {title: 'name', name: 'Mirazim',show: false},
                {title: 'name', name: 'Dilmurod',show: false},
                {title: 'name', name: 'Nafisa',show: false},
                {title: 'name', name: 'Ulug\'bek',show: false},
            ],
        }
    },
    methods: {
        delate: function() {
            this.boxItem.pop()
        },
        push: function() {
            this.boxItem.push(
                {title: 'name', name: 'Mirafzal',show: false}
            )
        }
    }
}
</script>

<style scoped>
.content {
    padding: 80px 100px;
    background-color: #055;
    display: flex;
    flex-wrap: wrap;
    position: relative;
}
.box{
    margin: 20px;
    flex-grow: 1;
    flex-basis: 350px;
    height: 250px;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    background-color: rgb(114, 19, 204);
    border: 2px solid red;
    cursor: pointer;
    color: #fff;
}
.title{
    padding: 0 0 20px 0;
    /* color: #fff; */
}
.name{
    color: #fff;
     text-shadow: 22px 11px 18px rgb(255, 196, 0);
    font-size: 30px;
}
.button,
.push{
    width: 150px;
    height: 50px;
    background: rgb(7, 100, 100);
    color: #fff;
    font-size: 18px;
    border: 1px solid #111;
    outline: none;
    text-align: center;
    cursor: pointer;
}

.button {
    position: absolute;
    top: 10px;
    left: 300px;
}
.push{
    position: absolute;
    top: 10px;
    margin: 0 0 0 20px;
}
@media screen and (max-width:1200px) {
    .content{
        padding: 80px 80px;
    }
}
@media screen and (max-width:992px) {
    .content{
        padding: 80px 40px;
    }
}
@media screen and (max-width:576px) {
    .content{
        padding: 80px 20px;
    }
    .box{
        height: 200px;
    }
}
</style>