# AirConnect package for Synology NAS and Synology Router

A minimal Synology package for [AirConnect](https://github.com/philippe44/AirConnect
).

It allows you to use AirPlay to stream to UPnP/Sonos devices.

Currently it only runs the airupnp process with the following options:

```
airupnp-arm -b [router local ip]:49154 -z -l 1000:2000 -f /tmp/airupnp-arm.log -d all=error
```

The process is running with a low-privilege user.

## Tested devices

* Synology RT2600 router

## Build

```
make clean build
```

## Debugging

You can see the error logs by going to the Package Center and clicking **View Log** on the package's page.
If you want to see more logs then change the start command in scripts/start-stop-status and rebuild the package, then install it again.

## License

See https://github.com/philippe44/AirConnect/blob/master/LICENSE.