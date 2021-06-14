# Quantum-Simulator-Location-Selector

This solution solves a problem where physical locations need to be equipped with services or products to satisfy demand within a certain area, while minimizing costs. For example, selecting branch and ATM sites in banking domain, selecting locations for CCTVs or Air Quality sensors in cities, etc. For large instances(number of locations) this problem cannot be optimally solved classically as it becomes computationally complex and time-consuming. Simulated Quantum Annealing provides a better alternative to classical methods by drastically reducing the computing time while minimizing cost. It delivers the required parallelization to explore many possible combinations simultaneously.

## Input:
Supported content type: text/csv
Inputfile should be a csv file with not more then 200 datapoints.
File size should not exceed 300 KB
CSV file should contain a columns titled 'service', 'location', 'point', 'opening_costs', and 'equip_costs'.
## Output:
Content type: application/json
Final result is in json format with 3 keys 'service_allocation', 'enabled_locations' , and 'cost' .
Invoking endpoint
## AWS CLI Command
If you are using real time inferencing, please create the endpoint first and then use the following command to invoke it:

!aws sagemaker-runtime invoke-endpoint --endpoint-name $model_name --body fileb://$file_name --content-type 'text/csv' --region us-east-2 output.json

Substitute the following parameters:

"model-name" - name of the inference endpoint where the model is deployed
file_name - input zip file name
text/csv- type of the given input
output.json - filename where the inference results are written to
