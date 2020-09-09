---
title: People
permalink: /people/
---

{% assign people_sorted = site.people | sort: 'joined' %}
{% assign role_array = "pi|postdoc|phd|masters|RA|honor|alumni" | split: "|" %}

{% for role in role_array %}

{% assign people_in_role = people_sorted | where: 'position', role %}

<!-- Skip section if there's nobody -->
{% if people_in_role.size == 0 %}
  {% continue %}
{% endif %}

<div class="pos_header">
{% if role == 'pi' %}
<h3>Principal Investigator</h3>
 {% elsif role == 'postdoc' %}
<h3>Postdoctoral Fellows</h3>
 {% elsif role == 'phd' %}
<h3>Phd Students</h3>
 {% elsif role == 'masters' %}
<h3> Masters Students </h3>
 {% elsif role == 'RA' %}
<h3>Research Assistants</h3>
 {% elsif role == 'honor' %}
<h3>Honorary Members</h3>
 {% elsif role == 'alumni' %}
<h3>Alumni</h3>
{% endif %}
</div>

{% if role != 'alumni' %}
<div class="content list people">
  {% for profile in people_sorted %}
    {% if profile.position contains role %}
      <div class="list-item-people">
        <p class="list-post-title">
          {% if profile.avatar %}
            <a href="{{ site.baseurl }}{{ profile.url }}"><img class="profile-thumbnail" src="{{site.baseurl}}/images/people/{{profile.avatar}}"></a>
          {% else %}
            <a href="{{ site.baseurl }}{{ profile.url }}"><img class="profile-thumbnail" src="http://evansheline.com/wp-content/uploads/2011/02/facebook-Storm-Trooper.jpg"></a>
          {% endif %}
          <a class="name" href="{{ site.baseurl }}{{ profile.url }}">{{ profile.name }}</a>
        </p>
      </div>    
    {% endif %}
  {% endfor %}
</div>
<hr>

{% else %}


{% endif %}
{% endfor %}


### Collaborators

This is in no way a complete list of collaborators. If we've accidentally left you out and you would like to be linked, please send us an email.

**Harvard University:**
- [Sam Gershman - Dept of Psychology and Center for Brains, Minds, and Machines](http://gershmanlab.webfactional.com/people/sam.html){:target="_blank"}
- [Fiery Cushman - Dept of Psychology](https://psychology.fas.harvard.edu/people/fiery-cushman){:target="_blank"}
- [Natalia Vélez - Dept of Psychology](http://gershmanlab.webfactional.com/people/natalia.html){:target="_blank"}

**Princeton University:**
- [Mark Ho - Computational Cognitive Science Lab](https://markkho.github.io/){:target="_blank"}
- [Ishita Dasgupta - Computational Cognitive Science Lab](https://ishita-dg.github.io/){:target="_blank"}

**Max Planck Institutes:**

- [Eric Schulz - Max Planck Research Group: Computational Principles of Intelligence](http://cpilab.org/){:target="_blank"}
- [Björn Meder - Max Planck Institute for Human Development and University of Erfurt](https://bmeder.org/){:target="_blank"}
- [Jonathan Nelson - Max Planck Institute for Human Development and University of Surrey](https://www.jonathandnelson.com/){:target="_blank"}
- [Nico Schuck - Max Planck Research Group: Neurocode](https://schucklab.gitlab.io/){:target="_blank"}
- [Azzurra Ruggeri - Max Planck Research Group: iSearch](https://www.mpib-berlin.mpg.de/staff/azzurra-ruggeri.html){:target="_blank"}
- [Ralf Kurvers - Max Planck Institute for Human Development](https://www.mpib-berlin.mpg.de/person/93403){:target="_blank"}
- [Bernhard Spitzer - Max Planck Institute for Human Development](https://www.mpib-berlin.mpg.de/staff/bernhard-spitzer){:target="_blank"}
- [Alan Tump - Max Planck Institute for Human Development](https://www.mpib-berlin.mpg.de/staff/alan-novaes-tump){:target="_blank"}
- [Mona Garvert - Max Planck Institute for Human Cognitive and Brain Sciences](https://www.cbs.mpg.de/employees/garvert){:target="_blank"}

**University of College London:**
- [Maarten Speekenbrink - Computational Learning and Decision Making Lab](https://speekenbrink-lab.github.io/){:target="_blank"}

**University of Tübingen:**
- [Agnieszka Zuberer - Clinical Affective Neuroimaging Lab](https://scholar.google.com/citations?user=b1cBJ1EAAAAJ&hl){:target="_blank"}

**University of Konstanz:**
- [Wolfgang Gaissmaier - Social Psychology and Decision Sciences](https://www.spds.uni-konstanz.de/prof-dr-wolfgang-gaissmaier?page=1){:target="_blank"}
- [Wataru Toyokawa - Social Psychology and Decision Sciences](https://www.spds.uni-konstanz.de/dr-wataru-toyokawa){:target="_blank"}


**l'Université Côte d'Azur:**
- [Imen Bouhlel - Groupe de Recherche en Droit, Economie, Gestion](http://unice.fr/membres/tous-les-membres/gredeg/bouhlel-imen){:target="_blank"}
 
**University of Indiana, Bloomington:**
- [Rob Goldstone - Psychological and Brain Sciences](https://pcl.sitehost.iu.edu/rgoldsto/rob.html){:target="_blank"}


<!-- 
### Alumni

| Who are they | When were they here | Where they went |
| :------------- |:-------------| :-----------|
| [Steve Antos](http://kordinglab.com/people/steve_antos/index.html) | Graduate Student (2012 - 2019) | - |
| [Sofia Triantafillou](https://www.dbmi.pitt.edu/node/54091) | Postdoc (2016 - 2018) | Asst Prof. at University of Pittsburgh |
| [Gaiqing Kong](https://gaiqingkong.github.io/) | Visiting Scholar (2016 - 2018) | Postdoc at UCL |
| Claire Chambers | Postdoc (2015 - 2018) | - |

 -->
<br>