# tutorial Jekyll

Tutorial to create static website using jekyll

## Installation

### 1) Controller les requirements

1. Ruby: need version 2.5.0 or higher. To check if the version is good enough, use the command

    ```bat
    ruby -v
    ```

2. RubyGem Check your gem version using

    ```bat
    gem -v
    ```

3. Install it on ubuntu if Ruby and gem are not installed or recent enough

    ```bat
    sudo apt-get install ruby-full build-essential zlib1g-dev
    ```

Avoid installing RubyGems packages (called gems) as the root user. Instead, set up a gem installation directory for your user account. The following commands will add environment variables to your ~/.bashrc file to configure the gem installation path:

```bat
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

Finally, install Jekyll and Bundler:

```bat
gem install jekyll bundler
```

### 2) Set-up

Create a directory for your website.

Inside the directory, use the command:

```bat
bundle init
```

It will create a new Gemfile. We need to edit the file by adding:

```bat
Gem "jekyll"
```

Now everything is ready to create our first html file.

1. begin by creating an html file __index.html__ with the following code:

    ```html
    <!DOCTYPE html>
    <html>
    <head>
        <meta charset="utf-8">
        <title>Home</title>
    </head>
    <body>
        <h1>Hello World!</h1>
    </body>
    </html>
    ```

2. Build your website with the command:

    ```bat
    jekyll build
    ```

3. Run your server:

    ```bat
    jekyll serve
    ```

4. see your hello word message on http://localhost:4000

## Liquid

hello.