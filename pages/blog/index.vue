<template>
  <div style="padding: 40px 0;">
    <c-simple-grid
      :columns="{ sm: 2, lg: 3 }"
      class="app-container"
      mx="auto"
      spacing="8"
    >
      <PostItem
        v-for="(postData,postId) in postsData"
        :postData="postData"
        :key="postId"
      />
    </c-simple-grid>
  </div>
</template>

<script>
import { CSimpleGrid } from '@chakra-ui/vue'
import PostItem from '@/components/blog/PostItem'
import { mapGetters } from 'vuex'
export default {
  computed: mapGetters({
    postsData: 'posts',
  }),
  components: {
    CSimpleGrid,
    PostItem,
  },
}
</script>

<style scoped></style>
