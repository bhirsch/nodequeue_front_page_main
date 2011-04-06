By default Civic installs the following nodequeues: 
- Featured Posts
- Featured Video
- Front Page Slideshow 
- Front Page Main

Nodequeues should really be installed and uninstalled by their parent modules. 
(Hopefully one day they will be exportable, which will make this process a lot 
cleaner.) But these four queues don't clearly belong to any one module. To 
start untangling them, the install profile will now create these queues
by turning on these four simple modules, whose sole purpose is to create
and delete nodequeues on hook_install and hook_uninstall.

- nodequeue_featured_posts
- nodequeue_featured_video
- nodequeue_front_page_slideshow
- nodequeue_front_page_main

Now, any (or all) of these queues can be cleanly, easily disabled by 
uninstalling the corresponding module. These modules can also be set as 
dependencies in any feature that needs them.
