**adenias@adenias-aspirev5471**:**\~/Downloads/cli-confluent/desafio-final**\$ export ENV=\$(confluent environment list \-o json \| python3 \-c "import json,sys;print(\[e\['id'\]for e  
in json.load(sys.stdin) if e \['name'\]=='desafio-final'\]\[0\])")

**adenias@adenias-aspirev5471**:**\~/Downloads/cli-confluent/desafio-final**\$ confluent environment use \$ENV  
Using environment env-713m11.

**adenias@adenias-aspirev5471**:**\~/Downloads/cli-confluent/desafio-final**\$ confluent environment list  
 Current \|     ID     \|     Name      \| Stream Governance Package     
\----------+------------+---------------+----------------------------  
         \| env-3kq7k0 \| default       \| ESSENTIALS                    
 \*       \| env-713m11 \| desafio-final \| ESSENTIALS   

**adenias@adenias-aspirev5471**:**\~/Downloads/cli-confluent/desafio-final**\$ confluent environment use env-713m11      
Using environment env-713m11.  
**adenias@adenias-aspirev5471**:**\~/Downloads/cli-confluent/desafio-final**\$ export CLUSTER=\$(confluent kafka cluster list \--environment env-713m11 \-o json \\  
 \| jq \-r '.\[\] \| select(.name=="desafio-basic") \| .id')  
echo "\$CLUSTER"

