## Deploy Your Running Page in Various Platforms

### Linux Server

Recommend System: Ubuntu 20.04 LTS

Requirements: 

- Nginx or any other web servers;
- Python Environments (Anaconda is recommended);
- Nodejs (14) and Yarn (1.22.10 stable);

Steps:

1. Point your domain to your server;
2. Set your website root to `/public` folder; 
3. Use Anaconda create a Python environment with any name you want;
4. Follow the guide in `Installation` Part;
5. Done. Have fun with your Running Page!

### Github Pages

1. If you are using a custom domain for GitHub Pages, open [/.github/workflows/gh-pages.yml](https://github.com/yihong0618/running_page/blob/master/.github/workflows/gh-pages.yml), change `fqdn` to the domain of your site;

2. Modify `gatsby-config.js`, change `pathPrefix` to your own URL path. 

   Example: If the repository's name is `running_page`, then your Github Pages URL will be https://{yourname}.github.io/running_page , then the value will be `/running_page`;

3. Modify arguments in [`run_data_sync.yml`](https://github.com/yihong0618/running_page/blob/master/.github/workflows/run_data_sync.yml);
  1. Change `env` to your own app type and info;
    ![image](https://user-images.githubusercontent.com/15976103/94450124-73f98800-01df-11eb-9b3c-ac1a6224f46f.png)
  2. Add your secret in repo Settings > Secrets (add only the ones you need);
    ![image](https://user-images.githubusercontent.com/15976103/94450295-aacf9e00-01df-11eb-80b7-a92b9cd1461e.png)
    My secret is as follows
    ![image](https://user-images.githubusercontent.com/15976103/94451037-8922e680-01e0-11eb-9bb9-729f0eadcdb7.png)
  3. Add your [GitHub secret](https://github.com/settings/tokens) and have the same name as the GitHub secret in your project;
    ![image](https://user-images.githubusercontent.com/15976103/94450721-2f222100-01e0-11eb-94a7-ef1f06fc0a59.png)

4. Go to repository's `Actions -> Workflows -> All Workflows`, run `Data Sync` workflow first;

5. After that done, choose `Publish GitHub Pages` from the left panel, click `Run workflow`. Make sure the workflow runs without errors, and `gh-pages` branch is created;

6. Go to repository's `Settings -> GitHub Pages -> Source`, choose `Branch: gh-pages`, click `Save`. Then all done. Enjoy running!

### Vercel

1. Connect Vercel  to your GitHub repo;
![image](https://user-images.githubusercontent.com/15976103/94452465-2599b880-01e2-11eb-9538-582f0f46c421.png)

2. Import repo;
![image](https://user-images.githubusercontent.com/15976103/94452556-3f3b0000-01e2-11eb-97a2-3789c2d60766.png)

3. Awaiting completion of deployment;
4. Done. Enjoy Running!

### Cloudflare Pages

1. Click `Create a project` in `Pages` to connect to your Repo;
2. After clicking `Begin setup`, modify Project's `Build settings`;
3. Select `Framework preset` to `Gatsby`;
4. Scroll down, click `Environment variables`, input the variable below:
   > Variable name = `PYTHON_VERSION`, Value = `3.7`
5. Click `Save and Deploy`.
