# IXON Custom Component Workspace

Welcome to your workspace for developing custom components for the IXON Cloud. Note that creating custom components requires you to be able to write JavaScript or Typescript code, and that you are familiar with the [Node.js](https://nodejs.org/) ecosystem. Experience with a web framework such as [Vue](https://vuejs.org/) or [Svelte](https://svelte.dev/) will come in handy as well.

This workspace will contain the custom components that you've developed. You can check this workspace, with your custom components, into your preferred versioning system. To do so, you can download this repository as a ZIP file, or use `degit`, as shown below. You don't need to fork this repository, as the actual Software Development Kit (SDK) will be installed into your `node_modules`, and you can install updates using `npm` as you normally do. You can access the SDK via the `npm run` scripts, as shown later in this guide.

To create a new project based on this template using degit:
```sh
npx degit ixoncloud/component-workspace my-project
cd my-project
```

Note that you will need to have [Node.js](https://nodejs.org/) and [Git](https://git-scm.com/) installed.

## Getting started

Install the dependencies...

```sh
npm install
```

Now you can generate your first component. Choose a name for the component. It must be lowercase and cannot contain spaces or special characters. Dashes (`-`) may be used to break up words. For example `'my-component'`.

```sh
npm run generate my-component
```

You will be prompted to select a template. Upon completion, you will find the source files for your newly created component in the `/components` directory.

To actually view and test your component, run the following command...

```sh
npm run simulate my-component
```

...this opens the simulator app in a browser and builds your component in watch-mode, which means that any changes to the component source files will trigger a rebuild and will auto-reload the simulator.

## Documentation

To check out docs and examples on how to develop a custom component, visit [Custom Component Development Docs](https://cdn.ixon.cloud/custom-widgets/).

The [@ixon-cdk/runner](https://www.npmjs.com/package/@ixon-cdk/runner) page has a complete overview of all commands that can be run in a component workspace project.

## Deploying to the IXON Cloud

When your component is ready to be used in action, it can be deployed to the IXON Cloud. To do that, you must first log in with your IXON user account.

```sh
npm run login
```

Now that you're logged in, you can run the following command to deploy the component...

```sh
npm run deploy my-component
```

...You will be prompted for a company ID and page-component-template ID and whether you want to remember these settings to speed up the process for a next deployment.

If all goes well, the component gets uploaded to the platform and you'll receive a preview link. With this link you can test the component in production.

The final step is to publish the deployed component so that it becomes available to all company users...

```sh
npm run publish my-component
```

...You will be prompted to select a version out of a list of all unpublished versions up to the currently published version. Select the version you want to publish. If all goes well, it will now be available for all company users to use.
