<template>
  <main class="global_container">
    <H1>this is header</H1>
    <div>
      Sometimes people just say the meanest things lol awdawdawd Lorem ipsum
      dolor sit amet consectetur adipisicing elit. Libero illo quasi provident,
      obcaecati magni ipsa eligendi deserunt qui culpa earum consectetur
      doloribus praesentium et voluptas possimus facilis dolores labore
      veritatis?
      <ul id="array-rendering">
        <li v-for="item in items" :key="item.id">
          {{ item.name }}
          {{ item.level }}
          {{ item.class }}
          {{ item.status ? "Online" : "Offline" }}
        </li>
      </ul>
    </div>
    <h1>{{ counter }}</h1>
    <button id="btn" @click="handleClick">Click me</button>
  </main>
</template>
<script lang="ts">
type Data = {
  id: number;
  name: string;
  level: number;
  class: string;
  status: boolean;
};
const data: Data[] = [
  {
    id: 1,
    name: "Bob",
    level: 30,
    class: "Warrior",
    status: true,
  },
  {
    id: 2,
    name: "Esonas",
    level: 44,
    class: "Paladin",
    status: false,
  },
  {
    id: 3,
    name: "Rose",
    level: 55,
    class: "Mage",
    status: true,
  },
  {
    id: 4,
    name: "Jessie",
    level: 60,
    class: "Mage",
    status: false,
  },
];
export default {
  // eslint-disable-next-line @typescript-eslint/explicit-module-boundary-types
  data() {
 
    return {
      counter: 0,
      items: data,
    };
  },
  methods: {
    handleClick(): number {
      return (this.counter += 1);
    },
  },
};
</script>
