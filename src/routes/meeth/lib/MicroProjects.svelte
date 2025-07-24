<script>
  // Placeholder favorite stacks
  const stacks = [
    { name: 'Svelte', icon: '/src/lib/images/svelte-logo.svg' },
    { name: 'TypeScript', icon: '' },
    { name: 'Node.js', icon: '' },
    { name: 'Vite', icon: '' }
  ];

  // Placeholder micro projects
  const projects = [
    {
      name: 'Todo App',
      description: 'A simple todo list application built with Svelte.',
      link: 'https://github.com/example/todo-app'
    },
    {
      name: 'Weather Dashboard',
      description: 'Displays weather information using a public API.',
      link: 'https://github.com/example/weather-dashboard'
    },
    {
      name: 'Markdown Editor',
      description: 'A live markdown editor with preview.',
      link: 'https://github.com/example/markdown-editor'
    }
  ];
</script>

<div class="container">
  <div class="header text-3xl mb-4">My name is Meeth</div>

  <div class="section mb-6">
    <p class="text-2xl font-semibold mb-2">My Favorite Stacks</p>
    <div class="flex flex-wrap gap-4">
      {#each stacks as stack}
        <div class="stack-item flex items-center gap-2 p-2 border rounded shadow-sm bg-white">
          {#if stack.icon}
            <img src={stack.icon} alt={stack.name + ' logo'} width="28" height="28" />
          {/if}
          <span>{stack.name}</span>
        </div>
      {/each}
    </div>
  </div>

  <div class="section">
    <p class="text-2xl font-semibold mb-2">Micro Projects</p>
    <ul class="space-y-4">
      {#each projects as project}
        <li class="project-item border rounded p-4 bg-gray-50 hover:shadow-md transition">
          <div class="text-xl font-bold">{project.name}</div>
          <div class="text-gray-700 mb-2">{project.description}</div>
          <a class="text-blue-600 hover:underline" href={project.link} target="_blank" rel="noopener">View Project</a>
        </li>
      {/each}
    </ul>
  </div>
</div>

<style>
  .container {
    max-width: 700px;
    margin: 2rem auto;
    padding: 1.5rem;
    background: #f9fafb;
    border-radius: 12px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.04);
  }
  .header {
    text-align: center;
  }
  .section {
    margin-bottom: 2rem;
  }
  .stack-item {
    min-width: 110px;
    justify-content: center;
  }
  .project-item {
    background: #fff;
  }
</style>