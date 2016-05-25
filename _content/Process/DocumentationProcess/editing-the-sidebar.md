---
title: "Editing the sidebar"
---

## Example HTML

The sidebar is a manually controlled HTML file. Its location is Jekyll/_includes/sidebar.html

We have to manually update it. The code looks something like this:


{% highlight bash %}

<div class="catbloc-collection">
     <div class="catbloc">          
            <ul class="sidebar-post">


                  <h4>
                    <i class="fa fa-cog"></i>
                    Misc
                  </h4>
                  <li>
                        <a href="{{ site.contentsref }}Contents">
                         Contents
                        </a>
                  </li> 

                  <h4>
                  <i class="fa fa-folder"></i>
                  Test
                  </h4>                           
                   <li>
                        <a href="{{ site.contentsref }}SoftwareDevelopment-subtopics/ReviewAndCoaching">
                         Review and Coaching
                        </a>

                        <ul>
                            <a href="{{ site.contentsref }}SoftwareDevelopment-subtopics/SpecificationWriting">
                             Specification Writing
                            </a>

                            <li>
                                  <a href="{{ site.contentsref }}SoftwareDevelopment-subtopics/TestDeploy">
                                   Test Deploy
                                  </a>
                            </li>
                        </ul> 
                  </li>



               </ul>
            </div>
</div>

{% endhighlight %}


The first and last three lines should be left well alone. This is to do with the larger overall page structure.

#### Adding sections


We curate the bits inbetween. To start a new section add in:


{% highlight bash %}

<h4>
    <i class="fa fa-cog"></i>
    Misc
</h4>

{% endhighlight %}

We use [font awesome] to add icons next to section headers. At the time of writing they have 600+ icons. Use them!

#### Adding articles

Then add the articles you want. To specify a hierarchy nest the html. They should look like this:

{% highlight bash %}

<li>
	<a href="{{ site.contentsref }}Relative/Path/From/_content/Folder">
		Article Title
	</a>
</li>

{% endhighlight %}

Boom! You should now see your results.

[font awesome]: http://fontawesome.bootstrapcheatsheets.com/