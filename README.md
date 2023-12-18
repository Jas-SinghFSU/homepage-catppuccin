# Dracula for [Homepage](https://github.com/gethomepage/homepage) w/ [Icons](Dracula%20Icons)
  > A dark theme for [Homepage](https://github.com/gethomepage/homepage) with Dracula styled icons.

<p align="center">
  <img src="homepage-dracula.png?v=2" />
</p>

Additional icons are being worked on, please open a request issue if you would like certain icons faster. 

# Install
`docker-compose.yaml` example for the Homepage app
```yaml
version: "3"

services:
  homepage:
    image: ghcr.io/gethomepage/homepage:latest
    container_name: homepage
    ports:
      - 3000:3000
    volumes:
      - /path/to/config/directory:/app/config # Make sure your local config directory exists
      - /path/to/images/directory:/app/public/images # This is where your images/app-icons would go
      - /var/run/docker.sock:/var/run/docker.sock # (optional) For docker integrations
```

Be sure to modify the `custom.css` file in your `/path/to/config/directory` to apply the theme.

To change icons for your services/bookmarks, first put them in your `/path/to/images/directory` and map the directory as shown in the `docker-compose.yaml` example, restart the container and then refer to them as follows...

All icons can be previewed [here](icons-preview.md).

```yaml
- Portainer:
        href: https://portainer.yourdomain.com
        description: Streamlined container management software
        icon: /images/portainer.svg
        server: my-docker #if integrating with docker
        container: portainer #if integrating with docker
```
https://avatars.githubusercontent.com/u/21210205?v=4
# Team

| [![Jas Singh](https://github.com/Jas-SinghFSU.png?size=100)](https://github.com/Jas-SinghFSU) |
| ---------------------------------------------------------------------------------------- |
| [Jas Singh](https://github.com/Jas-SinghFSU)                                               |

## License

[MIT License](./LICENSE)
