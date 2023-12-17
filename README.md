# homepage-dracula
Dracula theme and icons for Homepage dashboard. (Work In Progress)

Docker Compose example for the Homepage app
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

To change icons for your services/bookmarks, first put them in your `/path/to/images/directory`, restart the container and then refer to them as follows...

```yaml
- Portainer:
        href: https://portainer.yourdomain.com
        description: Streamlined container management software
        icon: /images/portainer.svg
        server: my-docker #if integrating with docker
        container: portainer #if integrating with docker
```
