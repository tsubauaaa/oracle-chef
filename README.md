oracle Cookbook
===============
This cookbook makes your Oracle Database.

Requirements
------------
### Platforms
Oracle Linux 5.9~
### Oracle
Oracle Database 11g Release 2 (11.2.0.1.0)

### Deploy the Install Files
Both disk 1 and disk 2 should have been unzipped into the same database directory.
It stores the directory to files/default.

#### packages
- `toaster` - oracle needs toaster to brown your bagel.

Attributes
----------

#### oracle::default
<table>
  <tr>
    <th>Key</th>
    <th>Type</th>
    <th>Description</th>
    <th>Default</th>
  </tr>
  <tr>
    <td><tt>default['oracle']['setup']['hostname']</tt></td>
    <td>String</td>
    <td>hostname</td>
    <td><tt>ora-chef.tsubauaaa.com</tt></td>
  </tr>
  <tr>
    <td><tt>default['oracle']['setup']['packages']</tt></td>
    <td>Array</td>
    <td>requirement OS packages</td>
    <td><tt>%w{compat-libstdc++-33 libaio-devel unixODBC unixODBC-devel}</tt></td>
  </tr>
  <tr>
    <td><tt>default['oracle']['setup']['oinstall_gid']</tt></td>
    <td>Integer</td>
    <td>oinstall's group id</td>
    <td><tt>200</tt></td>
  </tr>
  <tr>
    <td><tt>default['oracle']['setup']['dba_gid']</tt></td>
    <td>Integer</td>
    <td>dba's user id</td>
    <td><tt>201</tt></td>
  </tr>
</table>

Usage
-----
#### oracle::default
Just include `oracle` in your node's `run_list`:

```json
{
  "name":"my_node",
  "run_list": [
    "recipe[oracle::default]"
  ]
}
```

Contributing
------------
TODO: (optional) If this is a public cookbook, detail the process for contributing. If this is a private cookbook, remove this section.

e.g.
1. Fork the repository on Github
2. Create a named feature branch (like `add_component_x`)
3. Write your change
4. Write tests for your change (if applicable)
5. Run the tests, ensuring they all pass
6. Submit a Pull Request using Github

License and Authors
-------------------
Authors: TODO: List authors
