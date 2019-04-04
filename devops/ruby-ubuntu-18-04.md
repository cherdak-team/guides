# Configure Ruby server using Ubuntu 18.04

1. [Initial Server Setup](https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-18-04)

2. [Install Rbenv and Ruby](https://www.digitalocean.com/community/tutorials/how-to-install-ruby-on-rails-with-rbenv-on-ubuntu-18-04) **(until the 4th step)**

3. [Install Nginx](https://www.digitalocean.com/community/tutorials/how-to-install-nginx-on-ubuntu-18-04-quickstart) **(until the 4th step)**

4. [Install Passenger](https://www.phusionpassenger.com/library/install/nginx/install/oss/bionic/)

5. Create site config

    - Create config file

        ```
        sudo nano /etc/nginx/sites-available/project-name.conf
        ```

        ```
        server {
                listen 80;
                listen [::]:80;

                server_name project-name.com www.project-name.com;
                root /var/www/project-name/current/public;

                passenger_enabled on;
        }
        ```

    - Enable site config

        ```
        sudo ln -s /etc/nginx/sites-available/project-name.conf /etc/nginx/sites-enabled/
        ```

    - Restart Nginx

        ```
        sudo systemctl restart nginx
        ```

6. [Install SSL certificate](https://www.digitalocean.com/community/tutorials/how-to-secure-nginx-with-let-s-encrypt-on-ubuntu-18-04) _(Redirect HTTP traffic to HTTPS)_

7. Deploy application using Capistrano
