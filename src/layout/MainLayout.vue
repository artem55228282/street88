<template>
  <div class="wrapper">
    <div class="header">
      <div class="container">
        <div class="header-top">
          <logo />
          <div class="header-top-nav">
            <ul>
              <li>
                <a href="" class="cart">Корзина <span>0</span></a>
              </li>
              <li><a href="">Меню</a></li>
              <li><a href="">О нас</a></li>
              <li><a href="">Контакты</a></li>
            </ul>
          </div>
        </div>
        <div class="header-content">
          <h1>Большой гамбургер</h1>
          <span>говядина</span>
          <p class="description">
            Свежая хрустящая булочка, листики салата, маринованный огурец с
            луком и небольшая котлета, сдобренная майонезом и кетчупом, - таков
            классический портрет гамбургера, наиболее распространенной «быстрой»
            еды в США, от отравления которой ежедневно на больничных койках
            оказываются десятки тысяч американцев
          </p>
          <a class="header-content-price col-4">14 500</a>
        </div>
        <router-view />
      </div>
    </div>
  </div>
</template>

<script>
import Logo from "../components/Logo.vue";
export default {
  name: "MainLayout",
  components: {
    Logo,
  },
};
</script>

<style lang="scss" scoped>
$main-color: #69cf17;
$second-color: #dedede;
$white-color: #ffffff;
$font-raleway: "Raleway";
$font-roboto: "Roboto";

.header {
  width: 100%;
  background-image: url("../assets/header-bg.png");
  background-repeat: no-repeat;
  background-size: cover;
  min-height: 768px;
  .container {
    .header-top {
      padding-top: 30px;
    }
  }
}
.header-top {
  display: flex;
  justify-content: space-between;
  align-items: center;
  ul {
    align-items: center;
    display: flex;
    li {
      display: flex;
      align-items: center;
      transition: all 0.3s ease;
      a {
        display: inline-block;
        padding: 12px 15px 15px;
        font-family: $font-raleway;
        color: $main-color;
        font-weight: 100;
      }
      &:hover {
        background: rgba($main-color, 0.5);
        a {
          color: $white-color;
        }
      }
    }
    .cart {
      span {
        padding: 0px 7px 3px;
        text-align: center;
        border-radius: 50%;
        font-family: $font-raleway;
        font-weight: 100;
        font-size: 20px;
        background: $white-color;
        color: $main-color;
      }
    }
  }
}
.header-content {
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  h1 {
    text-transform: uppercase;
    font-size: 72px;
    font-weight: 900;
    line-height: auto;
    font-family: $font-raleway;
    color: $main-color;
    margin-bottom: 0;
  }
  span {
    margin-top: -10px;
    font-family: $font-raleway;
    color: $main-color;
    font-size: 36px;
    font-weight: 400;
    text-transform: lowercase;
  }
  .description {
    margin-top: 30px;
    font-family: $font-raleway;
    font-weight: 400;
    color: $second-color;
    line-height: auto;
  }
  .header-content-price {
    margin-top: 75px;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 220px;
    height: 90px;
    padding-bottom: 10px;

    font-family: $font-raleway;
    font-weight: 100;
    font-size: 60px;
    color: $white-color;
    background: rgba($main-color, 0.5);
  }
}
</style>
