<template>
  <div class="Booksworld">
    <h1>{{title}}</h1>
    <p>{{price}}</p>
    <span v-if="sold">books out of stock</span>
    <ul>
      <li v-for="book in books">
        {{book.title}}
      </li>
    </ul>
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
        ]
    }
  }
}
</script>
