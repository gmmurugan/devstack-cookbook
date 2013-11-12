* devstack Cookbook
  
  Cookbook to install devstack
  
** Requirements
   
*** Cookbooks
    - git
      
*** Operating Systems
    - centos
    - ubuntu
      
** Attributes
   
   devstack::default
   
   
   | Key                                 | Type    | Description                                | Default         |
   |-------------------------------------+---------+--------------------------------------------+-----------------|
   | ~['devstack']['host-ip']~           | String  | The host/ip to bind the stack to           | ~198.101.10.10~ |
   | ~['devstack']['database-password']~ | String  | The password for the DevStack database     | ~ostackdemo~    |
   | ~['devstack']['rabbit-password']~   | String  | The password for tde rabbit service        | ~ostackdemo~    |
   | ~['devstack']['service-token']~     | String  | The token for the DevStack service user    | ~token~         |
   | ~['devstack']['service-password']~  | String  | The password for the DevStack service user | ~ostackdemo~    |
   | ~['devstack']['admin-password']~    | String  | The password for the DevStack admin user   | ~ostackdemo~    |
   | ~['devstack']['dest']~              | String  | The directory to install DevStack          | ~/opt/stack~    |
   | ~['devstack']['pip-timeout']~       | Integer | The default time out for pip               | ~1000~          |
   
   
   
** Usage
   
   devstack::default
   
   Just include ~devstack~ in your node's ~run_list~:
   
#+BEGIN_SRC json
  {
    "name":"my_node",
    "run_list": [
      "recipe[devstack]"
    ]
  }
#+END_SRC
   
** Contributing
   
   1. Fork the repository on Github
   2. Create a named feature branch (like `add_component_x`)
   3. Write your change
   4. Write tests for your change (if applicable)
   5. Run the tests, ensuring they all pass
   6. Submit a Pull Request using Github
      
** License and Authors
   
   Authors: Cameron Lopez
