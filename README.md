## Prerequisites 
[Docker](https://docs.docker.com/docker-for-mac/install/)

[Composer](https://getcomposer.org/)

## Usage

Clone this repository, go into the root of this project:
```
git clone https://github.com/pardamike/docker-compose-laravel.git
cd docker-compose-laravel
```

Next, build Docker
```
docker-compose build
```

Now lets run Docker
```
docker-compose up
```
*Note* To run Docker in the background, use the `-d` flag when running `docker-compose up`

Now, open up your browser of choice to [http://localhost:8080](http://localhost:8080) and you should see "It works!"

Next, to set up Laravel, delete the `public` folder and install Laravel into the `src` by running these commands (You do NOT need to stop Docker, you can do this while it is still running):
```
rm -r src/public
cd src/
composer create-project laravel/laravel .
```

Now go to [http://localhost:8080](http://localhost:8080) (or refresh the browser you had open already) and you should see Laravel running!

Your Laravel application now lives inside of the `src` folder

Containers created and their ports are as follows:

- **nginx** - `:8080`
- **mysql** - `:3306`
- **php** - `:9000`
