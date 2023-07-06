# Pi Blogging

This is a repository of a blog platform deployed on Raspberry Pi based on Hexo.

## How to deploy your own blogs

1. Boot your Raspberry Pi and connect it through `ssh` (Before connection, make sure the SSH function is turned on in Raspbian).

   ```
   ssh pi@169.254.151.137
   pi@169.254.151.137's password:
   ```

2. Use node.js to install Hexo.

   ```
   sudo apt-get install nodejs npm
   npm install -g hexo-cli
   ```

   Note that if you installed a low version of node.js through official source, Hexo would fail to install. It is recommended to change the download source.

   ```
   curl -fsSL https://deb.nodesource.com/setup_current.x | sudo -E bash -
   sudo apt-get install -y nodejs
   ```

3. Generate your blog space locally in Raspberry Pi.

   ```
   mkdir blog
   cd blog
   hexo init your_blog_name
   cd your_blog_name
   hexo g
   hexo serve
   ```

4. Access your blog through browser (for example, the generated address of my blogs is `http://169.254.151.137:4000`).

