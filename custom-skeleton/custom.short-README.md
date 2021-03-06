Note: This is a README template I put alongside specific openerp.buildout custom configuration I produce for my company's internal projects.


Installation instructions
=========================

1. Get openerp.buildout
-----------------------

Get a local copy of the openerp.buildout boilerplate:

        $ git clone git://github.com/kdeldycke/openerp.buildout.git
        $ cd ./openerp.buildout

As the repository above is subject to changes, freeze its code to the following stable revision:

        $ git checkout 6972b3f2ae37240c723355b5a1e50bc2270e3198


2. Use our specific configuration
---------------------------------

Follow instructions found in the `README.md` file, but skip the `git clone` step as we already performed it above.

In the `README.md` file, when it's time to update the `buildout.cfg` file, just skip that step.

Instead, download our specific configuration set at a frozen revision:

        $ svn export --username=mylogin --revision XXX --force https://svn.example.com/project/trunk/custom.buildout .

Then, when the `README.md` ask you to run `./bin/buildout`, use the following command instead:

        $ ./bin/buildout -c ./custom.cfg

After that you can proceed with the rest of instructions found in the `README.md` file.
