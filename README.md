# Huawei_Route_Limit_Utilization_TTP
How to calculate when a customer reaches route limit in Huawei NE40

In some scenarios you might need to identify if any customer reaches the route/prefix limit. With this repo, it can be realized automatically, and everyone will be informed with suspected customer.

#VRF Route Limit (prefix&route-table)

#
ip vpn-instance Customer_A
ipv4-family
  route-distinguisher 192.168.0.10:442
  import route-policy management-888-import
  tnl-policy lsp-lb
  prefix limit 100000 80
  vpn-target 11111:442 export-extcommunity
  vpn-target 11111:889 export-extcommunity
  vpn-target 11111:442 import-extcommunity
  vpn-target 11111:888 import-extcommunity
#

![image](https://user-images.githubusercontent.com/96883175/154515900-9b34db5f-d682-4ea8-b769-1b4f71b0afe8.png)
