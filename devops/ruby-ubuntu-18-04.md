# Configure Ruby server using Ubuntu 18.04

1. [Initial Server Setup](https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-18-04) with user `brownie` (or use [this script](https://www.digitalocean.com/community/tutorials/automating-initial-server-setup-with-ubuntu-18-04))

2. [Intall NodeJS with Yarn](https://www.digitalocean.com/community/tutorials/how-to-set-up-a-node-js-application-for-production-on-ubuntu-18-04) **(until the 3rd step)**

3. [Install Rbenv and Ruby](https://www.digitalocean.com/community/tutorials/how-to-install-ruby-on-rails-with-rbenv-on-ubuntu-18-04) **(until the 4th step)**

4. [Install Nginx](https://www.digitalocean.com/community/tutorials/how-to-install-nginx-on-ubuntu-18-04-quickstart) **(until the 4th step)**

5. [Install Passenger](https://www.phusionpassenger.com/library/install/nginx/install/oss/bionic/)

6. [Install PostgreSQL](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-18-04)

7. Deploy a project using [Capistrano](https://github.com/capistrano/capistrano)

8. Create site config

    1. Create config file

        ```
        sudo nano /etc/nginx/sites-available/project-name.conf
        ```

        ```
        server {
                listen 80;
                listen [::]:80;

                server_name project-name.com www.project-name.com;
                root /home/brownie/www/project-name/current/public;

                passenger_enabled on;
        }
        ```

    2. Enable site config

        ```
        sudo ln -s /etc/nginx/sites-available/project-name.conf /etc/nginx/sites-enabled/
        ```

    3. Restart Nginx

        ```
        sudo systemctl restart nginx
        ```

9. [Install SSL certificate](https://www.digitalocean.com/community/tutorials/how-to-secure-nginx-with-let-s-encrypt-on-ubuntu-18-04) _(Redirect HTTP traffic to HTTPS)_
