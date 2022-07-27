<template>
  <div id="app">
    <MyHeader :blocks="blocks" />
    <MyContent :headerHeight="headerHeight" :sections="sections" />
  </div>
</template>

<script>
import MyHeader from './components/MyHeader';
import MyContent from './components/MyContent';
export default {
  name: 'App',
  components: {
    MyHeader,
    MyContent,
  },
  data() {
    return {
      blocks: [
        {
          id: 1,
          name: 'Подборки',
          src: 'border-all-solid.svg',
        },
        {
          id: 2,
          name: 'Все категории',
          src: 'border-none-solid.svg',
        },
        {
          id: 3,
          name: 'Где поесть',
          src: 'cheese-solid.svg',
        },
        {
          id: 4,
          name: 'Что-то еще',
          src: 'martini-glass-empty-solid.svg',
        },
        {
          id: 5,
          name: 'И еще',
          src: 'utensils-solid.svg',
        },
      ],
      sections: [
        {
          header: 'Максимально сэкономить',
          section: [
            {
              id: 1,
              src: 'ga1.jpg',
              slogan: 'Акция Акция Sale!!!',
              brand: 'МегаФон',
              adress: 'Ростов на Дону, Большая Садовая улица, 63 (400м)',
              promotion: 'Акция',
            },
            {
              id: 2,
              src: 'ga2.jpg',
              slogan: 'Только сегодня распродажа!',
              brand: 'ЛЭтуаль',
              adress: 'Ростов на Донуая улица, 63 (400м) овая улица, 63 (250м)',
              promotion: 'Скидка до 10%',
            },
            {
              id: 3,
              src: 'ga3.jpg',
              slogan: 'Что-то в подарок при покупке Iphone',
              brand: 'МегаФон',
              adress: ', 63 (400м) ону, Большая Садовая улица, 63 (400м)',
              promotion: 'Акция',
            },
            {
              id: 4,
              src: 'ga4.jpg',
              slogan: 'Сервисы Appl Ростов на Дону',
              brand: 'МегаФон',
              adress: 'Ростов 63 (400м) ну, Большая Садовая улица, 63 (400м)',
              promotion: 'Скидка до 15%',
            },
            {
              id: 5,
              src: 'ga5.jpg',
              slogan: 'Сервисы Apple Ростов на Дону, Большая Садовая улица',
              brand: 'МегаФон',
              adress:
                'Ростов на До Ростов на Дону, Большая Садовая улица, 63 (400м)',
              promotion: 'Скидка до 20%',
            },
          ],
        },
        {
          header: 'Популярное сегодня',
          section: [
            {
              id: 1,
              src: 'ga6.jpg',
              slogan: 'Сервисы Apple в подарок при покупке Iphone',
              brand: 'МегаФон',
              adress:
                'Ростов на Дону, Большая Садовая у Ростов на Дону, 63 (400м)',
              promotion: 'Акция',
            },
            {
              id: 2,
              src: 'ga7.jpg',
              slogan: 'Сервисы Apple в подарок при покупке Iphone',
              brand: 'ЛЭтуаль',
              adress:
                'Ростов на Дону, Большая Садовая у Ростов на Дону, 63 (400м)',
              promotion: 'Скидка до 10%',
            },
            {
              id: 3,
              src: 'ga8.jpg',
              slogan: 'Сервисы Apple в подарок при покупке Iphone',
              brand: 'МегаФон',
              adress:
                'Ростов на Дону, Большая Садовая у Ростов на Дону, 63 (400м)',
              promotion: 'Акция',
            },
            {
              id: 4,
              src: 'ga9.jpg',
              slogan: 'Сервисы Apple в подарок при покупке Iphone',
              brand: 'МегаФон',
              adress:
                'Ростов на Дону, Большая Садовая у Ростов на Дону, 63 (400м)',
              promotion: 'Скидка до 15%',
            },
            {
              id: 5,
              src: 'animal1.jpg',
              slogan: 'Сервисы Apple в подарок при покупке Iphone',
              brand: 'МегаФон',
              adress:
                'Ростов на Дону, Большая Садовая у Ростов на Дону, 63 (400м)',
              promotion: 'Скидка до 20%',
            },
          ],
        },
        {
          header: 'Максимально сэкономить',
          section: [
            {
              id: 1,
              src: 'ga6.jpg',
              slogan: 'Сервисы Apple в подарок при покупке Iphone',
              brand: 'МегаФон',
              adress:
                'Ростов на Дону, Большая Садовая у Ростов на Дону, 63 (400м)',
              promotion: 'Акция',
            },
            {
              id: 2,
              src: 'ga7.jpg',
              slogan: 'Сервисы Apple в подарок при покупке Iphone',
              brand: 'ЛЭтуаль',
              adress:
                'Ростов на Дону, Большая Садовая у Ростов на Дону, 63 (400м)',
              promotion: 'Скидка до 10%',
            },
            {
              id: 3,
              src: 'ga8.jpg',
              slogan: 'Сервисы Apple в подарок при покупке Iphone',
              brand: 'МегаФон',
              adress:
                'Ростов на Дону, Большая Садовая у Ростов на Дону, 63 (400м)',
              promotion: 'Акция',
            },
            {
              id: 4,
              src: 'ga9.jpg',
              slogan: 'Сервисы Apple в подарок при покупке Iphone',
              brand: 'МегаФон',
              adress:
                'Ростов на Дону, Большая Садовая у Ростов на Дону, 63 (400м)',
              promotion: 'Скидка до 15%',
            },
            {
              id: 5,
              src: 'animal1.jpg',
              slogan: 'Сервисы Apple в подарок при покупке Iphone',
              brand: 'МегаФон',
              adress:
                'Ростов на Дону, Большая Садовая у Ростов на Дону, 63 (400м)',
              promotion: 'Скидка до 20%',
            },
          ],
        },
        {
          header: 'Популярное сегодня',
          section: [
            {
              id: 1,
              src: 'ga6.jpg',
              slogan: 'Сервисы Apple в подарок при покупке Iphone',
              brand: 'МегаФон',
              adress:
                'Ростов на Дону, Большая Садовая у Ростов на Дону, 63 (400м)',
              promotion: 'Акция',
            },
            {
              id: 2,
              src: 'ga7.jpg',
              slogan: 'Сервисы Apple в подарок при покупке Iphone',
              brand: 'ЛЭтуаль',
              adress:
                'Ростов на Дону, Большая Садовая у Ростов на Дону, 63 (400м)',
              promotion: 'Скидка до 10%',
            },
            {
              id: 3,
              src: 'ga8.jpg',
              slogan: 'Сервисы Apple в подарок при покупке Iphone',
              brand: 'МегаФон',
              adress:
                'Ростов на Дону, Большая Садовая у Ростов на Дону, 63 (400м)',
              promotion: 'Акция',
            },
            {
              id: 4,
              src: 'ga9.jpg',
              slogan: 'Сервисы Apple в подарок при покупке Iphone',
              brand: 'МегаФон',
              adress:
                'Ростов на Дону, Большая Садовая у Ростов на Дону, 63 (400м)',
              promotion: 'Скидка до 15%',
            },
            {
              id: 5,
              src: 'animal1.jpg',
              slogan: 'Сервисы Apple в подарок при покупке Iphone',
              brand: 'МегаФон',
              adress:
                'Ростов на Дону, Большая Садовая у Ростов на Дону, 63 (400м)',
              promotion: 'Скидка до 20%',
            },
          ],
        },
        {
          header: 'Максимально сэкономить',
          section: [
            {
              id: 1,
              src: 'ga6.jpg',
              slogan: 'Сервисы Apple в подарок при покупке Iphone',
              brand: 'МегаФон',
              adress:
                'Ростов на Дону, Большая Садовая у Ростов на Дону, 63 (400м)',
              promotion: 'Акция',
            },
            {
              id: 2,
              src: 'ga7.jpg',
              slogan: 'Сервисы Apple в подарок при покупке Iphone',
              brand: 'ЛЭтуаль',
              adress:
                'Ростов на Дону, Большая Садовая у Ростов на Дону, 63 (400м)',
              promotion: 'Скидка до 10%',
            },
            {
              id: 3,
              src: 'ga8.jpg',
              slogan: 'Сервисы Apple в подарок при покупке Iphone',
              brand: 'МегаФон',
              adress:
                'Ростов на Дону, Большая Садовая у Ростов на Дону, 63 (400м)',
              promotion: 'Акция',
            },
            {
              id: 4,
              src: 'ga9.jpg',
              slogan: 'Сервисы Apple в подарок при покупке Iphone',
              brand: 'МегаФон',
              adress:
                'Ростов на Дону, Большая Садовая у Ростов на Дону, 63 (400м)',
              promotion: 'Скидка до 15%',
            },
            {
              id: 5,
              src: 'animal1.jpg',
              slogan: 'Сервисы Apple в подарок при покупке Iphone',
              brand: 'МегаФон',
              adress:
                'Ростов на Дону, Большая Садовая у Ростов на Дону, 63 (400м)',
              promotion: 'Скидка до 20%',
            },
          ],
        },
      ],
      headerHeight: 0,
    };
  },
  mounted() {
    this.headerHeight = document.getElementById('my-header').offsetHeight;
  },
};
</script>

<style lang="scss">
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
html {
  font-family: 'Roboto', sans-serif;
  font-size: 16px;
  background: rgb(255, 247, 247);
}
.hide-horizontal-scrollbar {
  -ms-overflow-style: none;
  scrollbar-width: none;
  &::-webkit-scrollbar {
    display: none;
  }
}
</style>
