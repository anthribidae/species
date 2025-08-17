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
          <h2>Contributing Collections</h2>
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

          <ul>
            <li
              v-for="item in ASSISTANT_EDITORS"
              :key="item.person"
            >
              <span class="font-bold">{{ item.person }}</span> -
              {{ item.location }}
            </li>
          </ul>
          <h2>Developers</h2>
          <ul>
            <li
              v-for="item in DEVELOPERS"
              :key="item.person"
            >
              <span class="font-bold">{{ item.person }}</span> -
              {{ item.location }}
            </li>
          </ul>
          </div>
      </div>
      <OSFLogo
        class="hidden xl:block opacity-10 w-[40rem] text-primary-color absolute right-0 bottom-56 dark:text-base-content"
      />
    </div>
         </section>
</template>

<script setup>

const AUTHORS = [
  {
    person: 'K. Samanta Orellana',
    position: 'Author',
    location:
      'Biodiversity Institute and Natural History Museum, University of Kansas, USA'
  }
]

const CONTRIBUTORS = [
  {
    person: 'AMNH-',
    location: 'American Museum of Natural History, USA (Lee Herman)'
  },
  {
    person: 'ASUCOB-',
    location: 'OBrien Collection, Arizona State University, USA (Sangmi Lee)'
  },
   {
    person: 'ASUHIC-',
    location: 'Hasbrouck Insect Collection, Arizona State University, USA (Sangmi Lee)'
  },
  {
    person: 'CIPROC-',
    location:
      'Museo de Insectos, Universidad de Costa Rica, Costa Rica (Andrés Arias, Humberto Lezama)'
  },
  {
    person: 'KUNHM-',
    location:
      'University of Kansas Biodiversity Institute and Natural History Museum, USA (Zack Falin, Rachel Osborn)'
  },
   {
    person: 'MNCR-',
    location: 'Museo Nacional de Costa Rica, former INBio, Costa Rica (Marianela Cambronero)'
  },
  {
    person: 'NMNH-',
    location: 'Smithsonian National Museum of Natural History, USA (Lourdes Chamorro)'
  },
   {
    person: 'NZAC-',
    location: 'New Zealand Arthropod Collection, New Zealand (Richard Leschen, Grace Hall)'
  },
  {
    person: 'SSAC-',
    location: 'Salvatore S. Anzaldo Research Collection, USA (Salvatore S. Anzaldo)'
  },
  {
    person: 'UCRG-',
    location:
      'Universidad de Costa Rica, Sede Guanacaste, Costa Rica (Jairo Mora)'
  }
]

const DEVELOPERS = [
   {
    person: 'TaxonPages',
    location: 'TaxonPages Working Group'
  }
]
</script>
