# Anshiro
<p>Start a nginx container with ansible and select the web project</p>

**ansible 2.7.9**
<br />
**Docker version 18.09.4**
### Getting Started
<p>First of all prepare yours files .html in a directory and then we can start it.</p>
<br />
1. Execute the git clone of project
<br />

```bash
git clone https://github.com/Heavyrocky/anshiro.git
```
<br />

```bash
sudo vim <path>/anshiro/playbooyk.yml
```
<br />
2. Inside of this file playbook.yml change the path of template's html that have kept in directory, editing the variable {{" site "}}

<br />

3. After saved, use the command

<br />

```bash
ansible-playbook playbook.yml --tags "<tags>" -e "container_name=<container_name>"
```
<br />
`--tags` : parameter useful to be able to run only a specific part of it rather than running everything in the playbook <br />

`-e "container_name"` : parameter used to set the name of container

</p>

### Instructions

<p>
Use ansible tags to select with tasks that can be use. 
<br />
</p>

#### Tags:
<br />
<p>
*create_directory*: create a directory where the html's template will be allocated 
<br />
*create_container*: create a container with nginx's image
<br />
*file_1*: first template's archive that will be launched on nginx
<br />
*file_2*: alternative template that will be changed with the first
<br />
*restart_container*: restart the container service
<br />
</p>

#### Vars:
<br />
<p>
*site*: path of file <yoursite>.html
<br />
*container_name*: name of container that can be created
<br />
</p>
