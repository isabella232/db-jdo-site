# db-jdo-site
Sources for the Apache DB JDO web site

While under construction, the website can be found under [https://apache.github.io/db-jdo-site/](https://apache.github.io/db-jdo-site/) 

This repository contains the JDO website source.

 * The ASCIIDOC sources can be found in `src/main/asciidoc`
 * The website menu is defined in `src/main/template`
 * The converter for migrating the old html files to asciidoc can be found in `src/main/java`



How to build the website:
 * Use `git pull`  to get the latest version from the repository.
 * Use `git branch MyBranchName` and `git checkout MyBranchName` to create a branch and check it out.
 * Adapt the asciidoc files in `src/main/asciidoc` or the website menu in  `src/main/template`
 * Call `mvn clean compile`. This generates html files in `target/site`. 
 * Copy all files from `target/site` into the `docs` folder, do not forget subfolders.
 * Verify the generated website by viewing it locally with a web browser. 
 * Commit changes with `git commit -m 'my commit message' `.
 * Push changes to the repository with `git push`.
 * Go to Github.com and create a PR for your branch
 * Once the PR is accepted, the changes should be visible on the website (you may have to refresh the browser). 

How to add javadoc
* Create the javadoc jar (e.g. jdo-api-3.2-javadoc.jar) in the db-jdo repository by calling `mvn clean install -Papache-release` in the api submodule.
* Create a new folder under docs e.g. docs/api32.
* Copy the javadocs jar info the new folder: e.g. `cp  jdo-api-3.2-javadoc.jar  docs/api32`.
* Create a new subforder docs/api32/jdo-api-3.2-javadoc
* Unpack the javadoc jar in the subfolder
* Edit javadoc.adoc under src/main/asciidoc and create a new section 'JDO 3.2 javadoc'.
* Add two links: one referring index.html in the subfolder and one referring the javadoc jar.

### TODO Documentation
 * General -> Downloads: Link to release-3.1? Add section about previous releases, 3.0.1 etc?
 * JDO Implementation -> Specification: Where do we host the PDF files?
 * Development -> Sourcecode page
 * Development -> Coding standard page
 * Community -> Team/Organizations
 * Development -> Dependencies (SVN -> Git)
 * Consider removing jdocentral.adoc / newshistory.adoc
 * Cleanup everything
 
### TODO Process
 * Set output folder to `output` or `content` (for use by `.asf.yaml`)
 
