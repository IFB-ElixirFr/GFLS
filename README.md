# GFLS (Galaxy For Life Science)  :heavy_minus_sign::sparkles::sparkles::four::herb::microscope::heavy_minus_sign: BIOS4BIOL

##  :bar_chart: GFLS_Stats_Explorer :

This repository concern the **GFLS_Stats_Explorer** part of the GFLS project.
It is made in collaboration with the **statistics group of the CATI "BIOS4BIOL"**.
All the **R**, **Perl** and **XML** scripts are made by this team.

**[:heavy_exclamation_mark:Last Update]** We improved the wrappers with best practices of Galaxy community.
The dependencies are managed with Conda. 
Tools are avaible in the Toolshed (see below).
Tools are available on some French bioinformatics platform (see below).

---

* __The aim of the GFLS is to :__
  - **Enhance the wrappers** of the tools
  - **Package** their dependencies
  - Make them at disposition of everyone into different **instances** (Galaxy servers, Cloud)

* __There is 3+1 tool on this project :__
  - **summary_statistics** : This tool produces simple descriptive statistics from a numerical table. Statistical measures are computed for each column in the table. *:envelope: @contact melanie.petera[a]inra.fr*
  - **h_clust** : This tool allows to generate hierarchical cluster analysis on a numeric data table according to differents parameters. *:envelope: @contact luc.jouneau[a]inra.fr*
  - **pcaFactoMineR** This tool launch a Principal Component Analysis (PCA) as done in the FactoMineR package *:envelope: @contact marie.tremblay-franco[a]inra.fr*
  - **normalization** : This last one (the +1) was made during the GFLS project after an enhancement discussion of the differents tools with the stats group. It propose the user different normalization method to preprocess data tables (in tabular format). *:envelope: @contact luc.jouneau[a]inra.fr*

---

- __:envelope: Contacts :__
  - Manager of the GFLS project : *olivier.inizan[a]inra.fr*
  - Manager of the GFLS_Stats_Explorer *project : sarah.maman[a]inra.fr*
  - Developper for the GFLS project : *valentin.marcon[a]inra.fr*

---

- __:open_file_folder: Toolshed repository :__
  - **Summary Statistics** : [Toolshed](https://toolshed.g2.bx.psu.edu/repository/display_tool?repository_id=a22ecd1d534f115a&render_repository_actions_for=tool_shed&tool_config=%2Fsrv%2Ftoolshed%2Fmain%2Fvar%2Fdata%2Frepos%2F003%2Frepo_3762%2Fsummary_statistics.xml&changeset_revision=46ddb0591d8b)
  - **Hierarchical Clustering** : [Toolshed](https://toolshed.g2.bx.psu.edu/repository/display_tool?repository_id=130a7f992a413e74&render_repository_actions_for=tool_shed&tool_config=%2Fsrv%2Ftoolshed%2Fmain%2Fvar%2Fdata%2Frepos%2F003%2Frepo_3763%2Fh_clust.xml&changeset_revision=dc678d2c1976)
  - **PCAFactoMineR** [Toolshed)](https://toolshed.g2.bx.psu.edu/repository/display_tool?repository_id=637293c9fce67224&render_repository_actions_for=tool_shed&tool_config=%2Fsrv%2Ftoolshed%2Fmain%2Fvar%2Fdata%2Frepos%2F003%2Frepo_3764%2FpcaFactoMineR.xml&changeset_revision=7acfb3bdad66)
  - **Normalization** : [Toolshed](https://toolshed.g2.bx.psu.edu/repository/display_tool?repository_id=94d3cdf711399f29&render_repository_actions_for=tool_shed&tool_config=%2Fsrv%2Ftoolshed%2Fmain%2Fvar%2Fdata%2Frepos%2F003%2Frepo_3761%2Fnormalization.xml&changeset_revision=79f00bc83ecc)
  
  - **suite_statsexplorer_gfls_1_0** : [Toolshed](https://toolshed.g2.bx.psu.edu/repository?repository_id=6ef805e21b873090&changeset_revision=e86c42fe824d) (Allow you to install all four tools at a time)
  
- __:computer: Instance :__
  
  Tools are available on this instances (in the "statistics" category):
  - **Galaxy Sigenae/Genotool** : [http://sigenae-workbench.toulouse.inra.fr/galaxy/](http://sigenae-workbench.toulouse.inra.fr/galaxy/)
  - **Galaxy Migale** : [http://migale.jouy.inra.fr/galaxy/](http://migale.jouy.inra.fr/galaxy/)
  
---

---
  
##  :computer: Dev processus :

To work on this project you need to clone it (html or ssh way)

<code> git clone https://github.com/IFB-ElixirFr/GFLS.git # With html</code>

<code> git clone git@github.com:IFB-ElixirFr/GFLS.git     # With SSH</code>

<code> git fetch origin dev:dev # Get the "dev" branch</code>


#### Then, you will need to **follow the Versionning strategy** as descibed bellow :

![VersionningStrat](./Doc/VersionningStrat.bmp)

- ![#ff0000](https://placehold.it/10/ff0000/000000?text=+) **To make a change on a file, you need to create your own branch of developement ("Branch X"), based on the "Master" one.**

<code> git checkout master           # Change branch to Master</code>

<code> git pull origin master        # Recover the last changes</code>

<code> git checkout -b branchMyName  # Create a new branch named "branchMyNale" from the Master branch</code>

**or update your branch**

<code> git checkout branchMyName      # Change branch to your own </code>

<code> git pull origin master:master # Recover the last changes from Master</code>

- ![#ff0000](https://placehold.it/10/ff0000/000000?text=+) **Make your developement on your branch, and then commit and push to your branch**

<code> git commit -a -m "YourMessage" # Record changes to the repository</code>

<code> git pull origin branchYourName # EXCEPTIONAL : If another member use it to develop (or if you use several developement environment), recover the last changes in your branch </code>

<code> git push origin branchYourName # Push to the dev branch</code>

- ![#ff0000](https://placehold.it/10/ff0000/000000?text=+) **Merge with the "Dev" branch**

<code> git checkout dev       # Change branch to Dev</code>

<code> git pull origin dev    # Recover the last changes from Dev</code>

<code> git merge branchMyName # Merge your change with the dev branch</code>

- ![#ff0000](https://placehold.it/10/ff0000/000000?text=+) **If it's ok, push on the remote dev branch**

<code> git push origin dev            # Push to the dev branch</code>

- ![#ff0000](https://placehold.it/10/ff0000/000000?text=+)![#0000ff](https://placehold.it/10/0000ff/000000?text=+) : **Inform the administrator, and ask him to make the test with the dev branch if you are not able to**
- ![#0000ff](https://placehold.it/10/0000ff/000000?text=+) **Finally if the developement work, the administrator will push on the master branch**
- ![#0000ff](https://placehold.it/10/0000ff/000000?text=+) **The adminstrator will create a "tag" to the master node, corresponding to the new release of the project**

![#ff0000](https://placehold.it/10/ff0000/000000?text=+) Developer ![#0000ff](https://placehold.it/10/0000ff/000000?text=+) Admin




