<template>
<div>
    <div class="header">
        <img src="../assets/logo.png" alt="vue">
        <ul class="header_ul">
            <li v-for="headerItem in headerItems" :key="headerItem.header" class="header_li">
                <a href="#">{{ headerItem.header }}</a>
            </li>
        </ul>
    </div>
</div>
</template>

<script>

export default {
  data() {
    return {
        headerItems: [
            {header: "Home"},
            {header: "About"},
            {header: "Vue"}
        ]
    }
  }
}
</script>

<style scoped>
.header{
    background-color: #055;
    padding: 20px 100px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    border-bottom: 1px solid black;
}
.header img {
    width: 50px;
    height: auto;
}
.header_ul{
    display: flex;
    align-items: center;
    justify-content: center;
}
.header_li{
    padding: 0 0 0 20px;
    cursor: pointer;
    transition: all 0.7s;
}
.header_li a{
    color: #fff;
}
.header_li:hover a{
    color: #999;
}
@media screen and (max-width:1200px) {
    .header{
        padding: 20px 80px;
    }
}
@media screen and (max-width:992px) {
    .header{
        padding: 20px 40px;
    }
}
@media screen and (max-width:576px) {
    .header{
        padding: 20px 20px;
    }
}
</style>
