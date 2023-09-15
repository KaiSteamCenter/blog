# Mekhi's Blog 


<span style="color: cyan">**Welcome to my Blog!! Get ready for an exciting journey through the world of technology and development. We provide practical tutorials, industry insights, and creative explorations to empower your coding skills.**</span>

![Bootstrap Icon](/assets/bootstrapicon.png)

## Recent Posts
<ul>
    {% for post in site.posts %}
        <li>
            <a href="{{ post.url }}">{{ post.title }}</a>
        </li>
    {% endfor %}
</ul>