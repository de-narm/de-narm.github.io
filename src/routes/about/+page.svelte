<script lang="ts">
  import Textbox from "$lib/textbox.svelte"
</script>

<div class="flex flex-col gap-4">
  <Textbox
    title="The Club Behind the Software"
    blocks={[
      "Explorama is developed and maintained by Explorama e.V., a registered non-profit organization (eingetragener Verein) dedicated to creating accessible data analytics tools. As a community-driven club, we bring together developers, data enthusiasts, and subject matter experts who share a common vision.",
      "Our club operates on the principles of open source collaboration,transparency, and inclusivity. We believe in the power of community-driven development and the importance of making technology accessible to all.",
      "As a registered German non-profit organization (e.V.), we are committed to serving the public interest by providing free, open-source software that empowers people to work with data effectively.",
    ]}
  />
  <Textbox
    title="Support Open Source"
    blocks={[
      "Help us continue developing Explorama and making data analytics  accessible to everyone",
      "Use the Software: Download Explorama, explore its features, and integrate it into your workflow. Real-world usage helps us improve.",
      "Give Feedback: Share your experiences, report bugs, and suggest features. Your feedback guides our development priorities.",
      "Contribute Code: Join our development community. Fix bugs, add features, improve documentation, or help with translations.",
      "Support Us: Help sustain the project through donations or by joining Explorama e.V. as a member.",
    ]}
  />
  <Textbox
    title="Join Explorama e.V."
    blocks={[
      "Become a member of our club and be part of the community that shapes  the future of accessible data analytics. Members gain voting rights, participate in strategic decisions, and help guide the project's direction.",
    ]}
  >
    <a href="https://github.com/Explorama">Learn More About Membership</a>
  </Textbox>
</div>


