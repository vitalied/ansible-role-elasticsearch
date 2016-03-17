Ansible Role for Elasticsearch
==============================

[![Build Status](https://travis-ci.org/vitalied/ansible-role-elasticsearch.svg?branch=master)](https://travis-ci.org/vitalied/ansible-role-elasticsearch)
[![GitHub tag](https://img.shields.io/github/tag/vitalied/ansible-role-elasticsearch.svg)](https://github.com/vitalied/ansible-role-elasticsearch)
[![GitHub license](https://img.shields.io/github/license/vitalied/ansible-role-elasticsearch.svg)](https://github.com/vitalied/ansible-role-elasticsearch/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/ansible/role/10589.svg)](https://galaxy.ansible.com/vitalied/elasticsearch)

Ansible Role for Elasticsearch Management.

Requirements
------------

This role require Ansible 2.1 or higher.

This role was designed for Ubuntu Server 16.04 LTS.

Role Variables
--------------

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th>parameter</th>
<th>required</th>
<th>default</th>
<th>choices</th>
<th>comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>elasticsearch_version</td>
<td>yes</td>
<td>2.x</td>
<td><ul>
<li><code>2.x</code></li>
<li><code>etc...</code></li>
</ul></td>
<td>Version of Elasticsearch to install.</td>
</tr>
<tr class="even">
<td>elasticsearch_cluster_name</td>
<td>yes</td>
<td>my-application</td>
<td></td>
<td>Name of Elasticsearch cluster.</td>
</tr>
<tr class="odd">
<td>elasticsearch_node_name</td>
<td>yes</td>
<td>node-1</td>
<td></td>
<td>Name of Elasticsearch node.</td>
</tr>
<tr class="even">
<td>elasticsearch_node_rack</td>
<td>yes</td>
<td>r1</td>
<td></td>
<td>Name of Elasticsearch node's rack.</td>
</tr>
<tr class="odd">
<td>elasticsearch_data_dir</td>
<td>yes</td>
<td>/var/lib/elasticsearch</td>
<td></td>
<td>Specifies the data storage directory.</td>
</tr>
<tr class="even">
<td>elasticsearch_log_dir</td>
<td>yes</td>
<td>/var/log/elasticsearch</td>
<td></td>
<td>Name of Elasticsearch node's rack.</td>
</tr>
<tr class="odd">
<td>elasticsearch_bind_address</td>
<td>yes</td>
<td>_local_</td>
<td><ul>
<li><code>IP address</code></li>
<li><code>hostname</code></li>
<li><code><a href="https://www.elastic.co/guide/en/elasticsearch/reference/current/modules-network.html#network-interface-values">special value</a></code></li>
<li><code>an array of any combination of these</code></li>
</ul></td>
<td>
The IP address on which Elasticsearch will listen for requests.
<a href="https://www.elastic.co/guide/en/elasticsearch/reference/current/modules-network.html#common-network-settings">Network settings</a>
</td>
</tr>
<tr class="even">
<td>elasticsearch_port</td>
<td>yes</td>
<td>9200</td>
<td></td>
<td>The port on which Elasticsearch will listen for requests.</td>
</tr>
<tr class="odd">
<td>elasticsearch_plugins</td>
<td>no</td>
<td><code>[]</code></td>
<td><ul>
<li><code>[]</code></li>
<li><code>list</code></li>
</ul></td>
<td>List of Elasticsearch Plugins to install.</td>
</tr>
</tbody>
</table>

Dependencies
------------

No additional role dependencies.

Example Playbook
----------------

    - hosts: all
      roles:
        - role: vitalied.elasticsearch

License
-------

-   Code released under [MIT](https://github.com/vitalied/ansible-role-elasticsearch/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)
