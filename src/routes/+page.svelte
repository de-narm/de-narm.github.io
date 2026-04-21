<script lang="ts">
	import logo from '$lib/assets/logo.svg';
	import screenshot from '$lib/assets/screenshot.png';
	import Textbox from '$lib/textbox.svelte';

</script>

<!-- Main Block -->
<div class="w-full pt-20 flex-col flex justify-center items-center gap-6 
            relative">
  <!-- Intro Text -->
  <div class="w-[400px] text-center text-5xl font-semibold z-1">
    Data Analytics
    made <span class="text-logo italic">Simple</span>
  </div>
  <div class="w-3/4 text-center text-2xl font-medium text-stone-300 z-1">
    Analyze and visualize data without code. Explorama empowers subject matter experts to create dynamic visual stories with just a few clicks.
  </div>
  <button
    class="bg-logo px-5 py-3 rounded-xl z-1"
    href="https://github.com/Explorama/Explorama">
    Start now!
  </button>

  <!-- Screenshot -->
  <div class="mt-20 p-10">
    <div class="bg-zinc-950 p-4 border border-zinc-600 rounded-3xl">
      <img src={screenshot} class="rounded-2xl">
    </div>
  </div>

  <!-- Intro Text -->
  <Textbox
    title="What is Explorama?"
    blocks={[
      "Explorama is a user-friendly data analytics tool designed specifically for subject matter experts and individuals without in-depth technical knowledge. It enables data analysis and visualization without requiring coding skills or specialized technical training.",
      "Built with Clojure and ClojureScript, Explorama democratizes data analytics by making powerful analytical capabilities accessible to everyone.",
    ]}
  />

  <!-- Features -->
  <Textbox
    title="Key Features"
    blocks={[
      ["Mosaic:", "Display 10000+ Events and dig into your data via colors, grouping and sorting"],
      ["Map:", "Analyze your data geographically"],
      ["Charts:", "Visualize you aggregated data in charts"],
      ["Dashboards & Reports", ""]
    ]}
  />

  <!-- Example frame -->
  <div class="mt-20 px-10 relative w-full flex items-center">
    <div class="w-[650px] h-[400px] bg-frame-bg rounded-xl overflow-hidden 
                flex flex-col">
      <!-- Header -->
      <div class="w-full h-10 flex relative">
        <div class="w-2/3 h-full bg-frame-gray flex justify-end">
          <div class="h-full w-[200px] bg-frame-fill"
               style="clip-path: path('M 0 40 Q 50 40 100 20 Q 150 0 200 0 L 200 40');"
          >
          </div>
        </div>
        <div class="w-1/3 h-full bg-frame-fill">
        </div>
        <div class="absolute left-10 top-2">
          Some title
        </div>
      </div>

      <!-- Content -->
      <div class="w-full h-full border-y-3 border-frame-fill flex items-center 
                  justify-center">
                  Some pseudo interactive frame examples maybe?
      </div>

    </div>

    <!-- Example note -->
    <div class="absolute right-0 w-[350px] h-[200px] bg-zinc-400 rounded-4xl
                flex items-center justify-center text-black">
      Some Feature notes!
    </div>
  </div>

  <!-- Why Text -->
  <Textbox
    title="Why Explorama?"
    blocks={[
      ["Our Mission", ""],
      "We believe that powerful data analytics should not be limited to those with extensive technical backgrounds. Our mission is to democratize data analysis by creating tools that are accessible, intuitive, and powerful.",
      "Subject matter experts should be able to explore their data, discover insights, and make informed decisions without being held back by technical barriers. That's why we built Explorama.",
      ["Empowerment:", "Making data analytics available to everyone, regardless of technical skill"],
      ["Innovation:", "Pushing boundaries in user-friendly analytics software"],
      ["Community:", "Building together as an open-source community"],
    ]}
  />

  <!-- How Text -->
  <Textbox
    title="How to Use Explorama"
    blocks={[
      "Currently in alpha stage, Explorama is available in multiple formats to suit your needs.",
      "Browser Version Download and extract the Browser-build, then open the index.html file in Chrome or Edge. Perfect for quick access without installation.",
      "Desktop Version Native installers available for Windows and Linux. Built with Electron for a seamless desktop experience.",
      "Playground Try Explorama in a temporary analysis environment. Perfect for testing the platform before committing.",
    ]}
  />

</div>

