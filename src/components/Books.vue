<template>
  <div class="Booksworld">
    <h1 v-bind:style="styles">Welcome to the Book World</h1>
    <h1>{{title}}</h1>
    <p>{{price}}</p>
    <span v-if="sold">books out of stock</span>
    <ul>
      <li v-for="(book,index) in books" v-bind:key="index">
        {{book.title}}
      </li>
    </ul>
    <p>{{quantity}}</p>
    <input type="text" v-model="quantity"/>
  </div>
</template>

<script>
export default {
  name: 'BooksWorld',
  data (){
    return {
        title:'Word Bulid',
        price:250,
        sold: false,
        books:[
          {title: 'javascript'},
          {title: 'python'},
          {title: 'vuejs'}
        ],
        quantity:'5',
        styles:{
          backgroundColor:'red',
          fontSize:'40px'
        }
    }
  }
}
</script>


