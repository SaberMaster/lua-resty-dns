# new behavior dns resolver

## change info
impl the unix-like dns resolve method


1. search dns info from the first nameserver instread of random one
2. if the result receving from the nameserver is emtpy, will continue search the next one until all nameservers is searched or reach the max retry limit count.

## generate patch

`cddf8cd81cda5ff94e5aab26bb622f0384d0324a` is the last offical commit id

```
git diff cddf8cd81cda5ff94e5aab26bb622f0384d0324a HEAD > target.patch
```


## apply patch

apply patch to `{openresty-path}/lualib/resty/dns/resolver.lua`

or 

just copy `resolver.lua` file in this project to `{openresty-path}/lualib/resty/dns/resolver.lua`


