<template>
  <div class="flex flex-col mt-8">
    <div class="-my-2 py-2 overflow-x-auto sm:-mx-6 sm:px-6 lg:-mx-8 lg:px-8">
      <div
        class="
          align-middle
          inline-block
          shadow
          overflow-hidden
          sm:rounded-lg
          border-b border-gray-200
        "
      >
        <table class="min-w-full">
          <thead>
            <tr>
              <th
                class="
                  px-6
                  py-3
                  border-b border-gray-200
                  bg-gray-50
                  text-left text-xs
                  leading-4
                  font-medium
                  text-gray-500
                  uppercase
                  tracking-wider
                "
              >
                Category
              </th>
              <th
                class="
                  px-6
                  py-3
                  border-b border-gray-200
                  bg-gray-50
                  text-left text-xs
                  leading-4
                  font-medium
                  text-gray-500
                  uppercase
                  tracking-wider
                "
              >
                List Item
              </th>
              <th
                class="
                  px-6
                  py-3
                  border-b border-gray-200
                  bg-gray-50
                  text-left text-xs
                  leading-4
                  font-medium
                  text-gray-500
                  uppercase
                  tracking-wider
                "
              >
                Date
              </th>
              <th
                class="
                  px-6
                  py-3
                  border-b border-gray-200
                  bg-gray-50
                  text-left text-xs
                  leading-4
                  font-medium
                  text-gray-500
                  uppercase
                  tracking-wider
                "
              >
                Quantity
              </th>
             
            </tr>
          </thead>

          <tbody
            class=""
            v-for="(list, index) in lists"
            :key="index"
          >
            <tr>
              <td
                class="
                  px-6
                  py-4
                  whitespace-nowrap
                  border-b border-gray-200
                  items-center
                "
              >
                 {{ list.cat }}
              </td>
              <td class="px-6 py-4 whitespace-nowrap border-b border-gray-200">
                {{ list.text }}
              </td>

              <td class="px-6 py-4 whitespace-nowrap border-b border-gray-200">
                <!-- <div class="text-sm leading-5 text-gray-900"> -->
                {{ list.date }}
              </td>
              <td class="px-6 py-4 whitespace-nowrap border-b border-gray-200">
                {{ list.quantity }}
              </td>

              
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TeamData",

  data() {
    return {
      lists: [
        {
          cat: "Food",
          text: "Bag of rice",
          quantity: "2",
          date: "09/09/21",
          checked: false,
        },
        {
          cat: "Tech",
          text: "Surface Laptop 2",
          quantity: "2",
          date: "09/09/21",
          checked: false,
        },
        {
          cat: "School",
          text: "Surface Laptop 2",
          quantity: "2",
          date: "09/09/21",
          checked: false,
        },
      ],
      currentList: "",
    };
  },
  methods: {
    addList() {
      this.lists.push({ text: this.currentList, checked: false });
      this.currentList = "";
    },
    removeList(index) {
      this.lists.splice(index, 1);
    },
  },
};
</script>

