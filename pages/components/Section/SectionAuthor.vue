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
          <h3>Major Contributors</h3>
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
          <div class="flex flex-col justify-center items-center">
            <OSFLogo
              class="xl:hidden w-40 text-primary-color right-0 dark:text-base-content"
            />
            <p class="text-center">
              With the cooperation of
              <a
                class="whitespace-nowrap"
                href="https://orthsoc.org/"
                >The Orthopterists' Society</a
              >
            </p>
          </div>
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
    position: 'Project Author',
    location:
      'Biodiversity Institute and Museum of Natural History, University of Kansas, USA'
  }
]

const DEVELOPERS = [
  {
    person: 'José Luis Pereira',
    location: 'TaxonPages'
  }
]
</script>
