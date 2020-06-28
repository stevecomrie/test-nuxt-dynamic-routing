<template>
   <main>
      <p>
         Password Used: {{password}}<br>
         Data {{data}}
      </p>
   </main>
</template>

<script>
   export default {
      data: () => ({
         data: '',
         password : ''
      }),

      async asyncData ({ params }) {
         //let data = await fetch( CALL_TO_YOUR_API + params.id + '.json' ).then(res => res.json())
         let data = { fake : 'data', sample: 'returned from API' }

         return {
            data: data,
            password: params.id
         }
      }
   }
</script>
