<template>
  <section class="bg-base-foreground">
    <div class="container mx-auto p-4 sm:pb-10 relative box-border">
      <div class="prose !container dark:prose-invert">
        <h2>Authors</h2>
        <ul class="my-4">
          <li
            v-for="item in AUTHORS"
            :key="item.person"
          >
            <span class="block"
              ><span class="font-bold">{{ item.person }}</span> -
              {{ item.position }}</span
            >
            <span>{{ item.location }}</span>
          </li>
        </ul>

        <div>
          <h3>Contributing Collections</h3>
          <ul>
            <li
              v-for="item in CONTRIBUTORS"
              :key="item.person"
            >
              <span class="font-bold">{{ item.person }}</span> -
              {{ item.location }}
            </li>
          </ul>
        </div>
        <div class="my-4">
          <h3>Assistant editor</h3>
          <ul>
            <li
              v-for="item in ASSISTANT_EDITORS"
              :key="item.person"
            >
              <span class="font-bold">{{ item.person }}</span> -
              {{ item.location }}
            </li>
          </ul>
          <h3>Developers</h3>
          <ul>
            <li
              v-for="item in DEVELOPERS"
              :key="item.person"
            >
              <span class="font-bold">{{ item.person }}</span> -
              {{ item.location }}
            </li>
          </ul>
          <hr class="border-b-base-border" />
          </div>
        </section>
</template>

<script setup>

  const AUTHORS = [
  {
    person: 'K. Samanta Orellana',
    position: 'Project Author',
    location:
      'Biodiversity Institute and Museum of Natural History, University of Kansas, USA'
  }
]

  const CONTRIBUTORS = [
  {
    person: '(ASUCOB, ASUHIC) Arizona State University Biocollections ',
    location: 'Dr. Sangmi Lee'
  },
  {
    person: '(KUNHM) University of Kansas Biodiversity Institute and Natural History Museum',
    location:
      'Dr. Zack Falin and Dr. Rachel Osborn'
  },
  {
    person: '(NZAC) New Zealand Arthropod Collection',
    location:
      'Dr. Rich Leschen'
  }
]
const DEVELOPERS = [
  {
    person: 'José Luis Pereira',
    location: 'TaxonPages'
  }
]
</script>
