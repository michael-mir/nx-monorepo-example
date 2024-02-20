# Nx monorepo example

## How to run package scripts?

`yarn workspace {package} {script}`

## Generate code

If you happen to use Nx plugins, you can leverage code generators that might come with it.

Run `nx list` to get a list of available plugins and whether they have generators. Then run `nx list <plugin-name>` to see what generators are available.

Learn more about [Nx generators on the docs](https://nx.dev/plugin-features/use-code-generators).

## Running tasks

To execute tasks with Nx use the following syntax:

```
nx <target> <project> <...options>
```

You can also run multiple targets:

```
nx run-many -t <target1> <target2>
```

..or add `-p` to filter specific projects

```
nx run-many -t <target1> <target2> -p <proj1> <proj2>
```

Targets can be defined in the `package.json` or `projects.json`. Learn more [in the docs](https://nx.dev/core-features/run-tasks).

## Want better Editor Integration?

Have a look at the [Nx Console extensions](https://nx.dev/nx-console). It provides autocomplete support, a UI for exploring and running tasks & generators, and more! Available for VSCode, IntelliJ and comes with a LSP for Vim users.

## Ready to deploy?

Just run `nx build demoapp` to build the application. The build artifacts will be stored in the `dist/` directory, ready to be deployed.

## Set up CI!

Nx comes with local caching already built-in (check your `nx.json`). On CI you might want to go a step further.

- [Set up remote caching](https://nx.dev/core-features/share-your-cache)
- [Set up task distribution across multiple machines](https://nx.dev/core-features/distribute-task-execution)
- [Learn more how to setup CI](https://nx.dev/recipes/ci)

## Connect with us!

- [Join the community](https://nx.dev/community)
- [Subscribe to the Nx Youtube Channel](https://www.youtube.com/@nxdevtools)
- [Follow us on Twitter](https://twitter.com/nxdevtools)

The component also supports many properties for more specific work:
| **Prop**                  | **Type** | **Default**  | **Note**                                                                                |
| ------------------------- | -------- | ------------ | --------------------------------------------------------------------------------------- |
| stream                    | boolean  |              | external media stream (turns off internal media stream handling logic)                  |
| mirrored                  | boolean  | false        | show camera preview and get the screenshot mirrored                                     |
| mainCamera                | boolean  | false        | should use a main camera (requires Navigator.mediaDevices.enumerateDevices)             |
| frontCamera               | boolean  | false        | should use a front camera (MediaTrackConstraints['facingFront'] === 'user')             |
| applyConstraints          | boolean  | false        | should new constraints be applied to the media stream                                   |
| cameraResolutionType      | string   |              | video track resolution size - `('UHD' \| 'QHD' \| 'FHD' \| 'HD')`                       |
| cameraResolutionMode      | string   | 'ideal'      | video track resolution mode - `('min' \| 'max' \| 'ideal' \| 'exact')`                  |
| audioConstraints          | object   |              | audio track constraints - MediaStreamConstraints['audio']                               |
| videoConstraints          | object   |              | video track constraints - MediaStreamConstraints['video']                               |
| requestTimeLimit          | number   |              | limiting the media stream request by time                                               |
| onStreamRequest           | function |              | callback for when component requests a media stream                                     |
| onStreamStart             | function |              | callback for when component starts a media stream                                       |
| onStreamStop              | function |              | callback for when component stops a media stream                                        |
| onStreamError             | function |              | callback for when component can't receive a media stream                                |
