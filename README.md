# Laravel 5.8 with a Docker PHP Image

A demo repo for deploying a Laravel PHP application on [Render](https://render.com) using Docker. You can follow the getting started tutorial [here](https://render.com/docs/deploy-php-laravel-docker).


<p dir="auto"><a href="https://deploy.cyclic.app/" rel="nofollow"><img src="https://camo.githubusercontent.com/9c27ca7ef5947882143d1c04145ac1341dc7088b908d07bcbceab3c240d0456a/68747470733a2f2f6465706c6f792e6379636c69632e6170702f627574746f6e2e737667" alt="Deploy to Cyclic" data-canonical-src="https://deploy.cyclic.app/button.svg" style="max-width: 100%;"></a></p>
## Deployment

1. [Create](https://dashboard.render.com/new/database) a new PostgreSQL database on Render and copy the internal DB URL to use below.

2. Fork this repo to your own GitHub account.

3. Create a new **Web Service** on Render, and give Render's GitHub app permission to access your new repo.

4. Select `Docker` for the environment, and add the following environment variable under the *Advanced* section:

   | Key             | Value           |
   | --------------- | --------------- |
   | `DATABASE_URL`  | The **internal connection string** for the database you created above. |
   | `DB_CONNECTION`  | `pgsql` |
   | `APP_KEY`  | Copy the output of `php artisan key:generate --show` |

That's it! Your Laravel 5.8 app will be live on your Render URL as soon as the build finishes. You can test it out by registering and logging in.
