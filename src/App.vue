<script setup>
import { CheckCircleIcon } from '@heroicons/vue/24/solid'
import { ClockIcon, ListBulletIcon, ChartBarIcon } from '@heroicons/vue/24/outline'

const navItems = ['timeline', 'activities', 'progress']
</script>

<template>
  <header class="sticky top-0 z-20 flex items-center justify-between border-b bg-white p-3">
    <a href="#">
      <img src="./assets/logo.png" alt="logo" class="h-9">
    </a>
    <a href="#" class="text-sm">
      <div class="flex items-center gap-1">Day complete
        <CheckCircleIcon class="h-7 text-green-500" />
      </div>
      <div class="flex items-center gap-1">
        <div class="">Progress: <span class="font-mono">20%</span></div>
        <div class="h-3 w-3 rounded-full bg-red-500"></div>
      </div>
    </a>
  </header>

  <!-- <main class="flex flex-grow flex-col">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Minus omnis accusantium quas harum alias non explicabo excepturi animi quia? Quam debitis nihil obcaecati. Quod aut quasi, sed eaque odio recusandae soluta repellat quidem quos exercitationem eius pariatur unde quam odit, amet neque ab temporibus voluptatem impedit ipsa non porro? Voluptatem veniam cumque nam. Id consectetur sit accusantium blanditiis corporis neque optio quo ut. Ad nostrum magnam consequuntur sit voluptate veritatis error minima commodi dolore, aliquam placeat aperiam nulla expedita, tempora, ratione repellendus delectus quas hic neque. Minus commodi facilis odit. Dolor dolorem at porro optio eius animi ab neque, natus, reprehenderit repellat tempore, earum voluptatibus repellendus dolore? Ea dignissimos quasi nulla sequi repellendus laborum, esse ipsa eos tempora, necessitatibus officia nisi blanditiis quaerat nesciunt debitis nostrum voluptas deserunt ab praesentium impedit nobis repudiandae magnam. Debitis, doloremque ipsum rem, quia, repellendus impedit quasi accusamus ratione ea delectus illo quibusdam voluptatem aliquam inventore. Facilis, repudiandae molestiae qui aliquid provident expedita sequi, reprehenderit sint labore in reiciendis tempore iure dolor minima hic animi libero eum doloremque minus a doloribus amet veritatis. Sequi blanditiis quis reprehenderit officiis recusandae libero repellat nihil enim, eius voluptatibus reiciendis similique dolore vitae non dolor ducimus cupiditate velit molestias maxime impedit et totam fuga? Labore, autem quo quia distinctio non nobis deleniti quasi maiores impedit molestiae voluptatem, magnam velit neque esse praesentium? Impedit voluptatum quasi nostrum adipisci quis, quibusdam est, tempora eos culpa laboriosam, molestiae maiores cum maxime officia perspiciatis reprehenderit sunt distinctio consectetur? Dicta, voluptatem hic exercitationem voluptatum nihil commodi necessitatibus sunt eveniet, aspernatur aliquam architecto temporibus voluptatibus iusto tenetur ea accusantium quas quam velit praesentium iste, mollitia quod quaerat delectus provident. Consequatur enim porro, ullam aliquid placeat molestias facilis. Earum necessitatibus blanditiis architecto iure repellat officia, exercitationem omnis expedita dolor mollitia odit? Tempora, nulla? Veritatis, reprehenderit expedita.</main> -->
  
  <nav class="sticky bottom-0 z-10 bg-white text-3xl">
    <ul class="flex items-center justify-around">
      <li v-for="page in navItems" :key="page" class="flex-1">
        <a :href="`#${page}`" class="flex flex-col items-center p-2 text-xs capitalize">
          <ClockIcon v-if="page === 'timeline'" class="h-6 w-6"/>
          <ListBulletIcon v-else-if="page === 'activities'" class="h-6 w-6"/>
          <ChartBarIcon v-else class="h-6 w-6"/> {{ page }}
        </a>
      </li>

      <!-- <li class="flex-1">
        <a href="#activities" class="flex flex-col items-center p-2 text-xs capitalize"><ListBulletIcon class="h-6 w-6"/>activities</a>
      </li>
      <li class="flex-1">
        <a href="#progress" class="flex flex-col items-center p-2 text-xs capitalize"><ChartBarIcon class="h-6 w-6"/>progress</a>
      </li> -->
    </ul>
  </nav>
</template>

<style scoped></style>
