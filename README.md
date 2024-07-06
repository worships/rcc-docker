# RCC In Docker
A set of simple docker files to easily run RCCService (Roblox Cloud Compute Platform) as a container.


## Info
There are two provided folders, Linux, and Windows. These are the seperate image types. If you cannot for some reason run windows containers natively, you can simply use the linux one.

> Please note that, RCCService is not provided here, you will have to source it yourself. There are plenty of places you can find RCC. It must be placed in the RCC directory.

> This is setup only if you are planning to use RCC as a SOAP server, which is recommended.

## Setup
If you plan to use ***native windows***:
```bash
docker build -t rcc-windows -f Dockerfile.windows .

docker run -p 64989:64989 -p 53640-53900:53640-53900 rcc
```

Or if you plan to use ***linux running wine***:
```bash
docker build -t rcc-linux -f Dockerfile.linux .

docker run -p 64989:64989 -p 53640-53900:53640-53900 rcc-linux
```

> Please keep in mind that the linux image is running RCC in **wine**, which may lead to performance or compatability issues.
> There will be output errors from wine related to display issues, ignore these, RCC will work eitherway.