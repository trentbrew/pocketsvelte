<script>
  import { onMount } from "svelte";
  import logo from "$lib/images/logomark.png";
  import pb from "$lib/pb/pocketbase.js";

  onMount(async () => {
    console.log("fetching test data...");
    const data = await pb.get("test");
    console.log("data: ", data);
  });
</script>

<main class="h-screen w-screen flex flex-col justify-center items-center">
  <img class="mb-6" width="100" src="{logo}" alt="logo" />
  <h1 class="text-3xl font-bold mb-2 shingo">Welcome to Docket.tv</h1>
  <p>The TV Guide for independent broadcasting</p>
</main>
