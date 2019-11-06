# Simple Pager Demo

This is a simple static pager I put together using [Svelte](https://svelte.dev). You can see it in action on [Zeit](https://public.robvince.now.sh).


The following is an excerpt of the documentation at [sveltejs/template](https://github.com/sveltejs/template). For more info
please check there.

___


To create a new project based on this template using [degit](https://github.com/Rich-Harris/degit):

```bash
npx degit rjvince/simple-pager-demo svelte-app
cd svelte-app
```

*Note that you will need to have [Node.js](https://nodejs.org) installed.*

Install the dependencies...

```bash
cd svelte-app
npm install
```

...then start [Rollup](https://rollupjs.org):

```bash
npm run dev
```

Navigate to [localhost:5000](http://localhost:5000). You should see your app running. Edit a component file in `src`, save it, and reload the page to see your changes.

## To Do

* Some kind of ellipsis function to handle pages that number more than a handful.