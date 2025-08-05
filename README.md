# Beacon

<p align="center">
  <img src="https://raw.githubusercontent.com/BeaconCMS/beacon/main/assets/images/beacon.png" width="256" alt="Beacon logo">
</p>

<p align="center">
  Beacon is a content management system (CMS) built with Phoenix LiveView. It brings the rendering speed benefits of Phoenix to even the most content-heavy pages with faster render times to boost SEO performance.
</p>

## Getting Started

Install both Phoenix and Igniter installers:

```sh
mix archive.install hex phx_new && mix archive.install hex igniter_new
```

Now you can either create a new Phoenix project with Beacon or add Beacon to an existing Phoenix project:

<details>
<summary>Create a new project</summary>

- Using latest published [beacon](https://hex.pm/packages/beacon) and [beacon_live_admin](https://hex.pm/packages/beacon_live_admin) packages:

```sh
mix igniter.new my_app --install beacon,beacon_live_admin --with phx.new --beacon.site my_site
```

- Or using the unreleased projects from GitHub from the main branch:

```sh
mix igniter.new my_app \
--install beacon@github:BeaconCMS/beacon,beacon_live_admin@github:BeaconCMS/beacon_live_admin \
--with phx.new \
--beacon.site my_site
```

Replace `my_app` and `my_site` with the names you want to generate and follow the prompts.

</details>

<details>
<summary>Add to existing project</summary>

If you already have a Phoenix project with Phoenix LiveView then you can just add Beacon into that project.

Similar to starting a new project, you can install Beacon and BeaconLiveAdmin and generate a new site:

- Using latest published [beacon](https://hex.pm/packages/beacon) and [beacon_live_admin](https://hex.pm/packages/beacon_live_admin) packages:

```sh
mix igniter.install beacon,beacon_live_admin --beacon.site my_site
```

- Or using the unreleased projects from GitHub from the main branch:

```sh
mix igniter.install \
beacon@github:BeaconCMS/beacon,beacon_live_admin@github:BeaconCMS/beacon_live_admin \
--beacon.site my_site
```

Replace `my_site` with the names you want to generate and follow the prompts.
</details>

To finish, install dependencies, run the server, and open http://localhost:4000 to see the default home page or http://localhost:4000/admin to manage your new site.

```sh
mix setup
mix phx.server
```

For more info, check out the [guides and recipes](https://hexdocs.pm/beacon/installation.html). If you're new to Beacon you can start with [Your First Site](https://hexdocs.pm/beacon/your-first-site.html) guide.

## Demo

A sample application running latest Beacon is available at https://github.com/BeaconCMS/beacon_demo

## Status

You can expect incomplete features and breaking changes before a stable v1.0 is released.

Main components:
- Core - A functional website can be built and deployed by inserting components in database and running a server, see https://github.com/BeaconCMS/beacon_demo
- Admin - LiveView UI to manage layouts, pages, and all other resources. See https://github.com/BeaconCMS/beacon_live_admin
- Page Builder - An easy to use, drag & drop UI for building pages, targeted to non-technical users. In the initial stages of development.

## Local Development

The file `dev.exs` is a self-contained Phoenix application running Beacon with sample data and code reloading enabled. Follow these steps to get a site up and running:

1. Install dependencies, build assets, and run database setup:

```sh
mix setup
```

2. Execute the dev script:

```sh
iex --sname core@localhost -S mix dev
```

Note that running a named node isn't required unless you're running Beacon LiveAdmin for local development as well.

Finally, visit any of the routes defined in `dev.exs`, eg: http://localhost:4001/dev or http://localhost:4001/dev/sample
