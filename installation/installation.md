# Installation

Now we have the correct repos configured, update the server with the latest updates from Red Hat.

```
yum -y update -y
```

Next we perform the actual installation:

# Satellite 6.0 and Satellite 6.1 installation:
```
yum install katello
```

# Satellite 6.2 and beyond installation:
```
yum install satellite
```
