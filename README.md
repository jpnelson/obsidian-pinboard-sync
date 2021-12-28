# Pinboard Sync

An Obsidian plugin that adds links you've saved with [Pinboard](Pinboard.in) to your Obsidian Daily Notes, synchronizing periodically.

## Why?

I've been using Pinboard to store links to interesting websites from the web for years, and from iOS devices with the help of the wonderful app [Pinner](http://pinnerapp.net).  I would like Obsidian to store these links as part of my Daily Notes to remind me to refer back to them, and also so that I can add some notes about each site.

## Disclaimer 🚨

The initial sync will backfill your recent posts from Pinboard into Obsidian. This potentially means creating/modifying up to a hundred files. I recommend testing this plugin out in a new vault first to make sure you're happy with the result.  You may not want Daily Notes with Pinboard links going that far back in time.

## Usage

This plugin will fetches recent links posted to your Pinboard and dumps them into the Daily Note corresponding to the date the link was stored.

It also displays any tags associated to the links.

It will refetch the posts at a designated interval.

## Settings

| Setting         | Description                                                                                      |
| --------------- | ------------------------------------------------------------------------------------------------ |
| Token           | API token from your Pinbord account.  Available in [settings/password](https://pinboard.in/settings/password)|
| Section Heading | Controls where the links will be displayed within your daily notes. Defaults to `## Pinboard`    |
| Sync Frequency  | How often you want to fetch the posts from the Pinboard API                                      |
| Tag Prefix      | You may prefix your Pinboard tags with a parent tag (e.g. `#pinboard/work` `#pinboard/school`)   |
| Recent Posts    | Number of recent posts to use when syncing.  Up tothe last 100 posts can be retreived.           |


## Limitations

This plugin currently only syncs the last xx posts, where xx <100.  Why?  I just switched over to using Obsidian from Roam, and I didn't want 1000 of Daily Notes that were only old Pinboard links.

This doesn't currently support "Pinboard Notes" because I never used those.

## Gratitude 🙏

This plugin was made possible by the awesome work by [liamcain](https://github.com/liamcain/obsidian-things-logbook) and [mrled](https://github.com/mrled/pinboardtool).  Thank you!


## Contributing

To make changes to this plugin, first ensure you have the dependencies installed.

```
yarn install
```

### Development

To start building the plugin with what mode enabled run the following command:

```
yarn dev
```

_Note: If you haven't already installed the hot-reload-plugin you'll be prompted to. You need to enable that plugin in your obsidian vault before hot-reloading will start. You might need to refresh your plugin list for it to show up._

### Releasing

To start a release build run the following command:

```
yarn build
```

---

<sub>This plugin was generated by (create-obsidian-plugin)[https://www.npmjs.com/package/create-obsidian-plugin]</sub>
