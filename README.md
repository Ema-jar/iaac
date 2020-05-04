# iaac

There are two different files:

 - **network**: emajar_network.yml
 - **services**: emajar_services.yaml

You should run the network script before, since the Outputs of this script are going to be used by the service script, those are the commands you can use:

 - ./create.sh emajarstacknetwork emajar_network.yml network_param.json
 - ./create.sh emajarstackservice emajar_service.yml service_param.json

The human readable URL starting with `http://` can be retrieved from the services Output.

For autoscaling group I've chosen the following size in order to speed up the process:
```
MinSize: '1'
MaxSize: '2'
```

You will probably have to create your own key inside your AWS account following this format: `KeyName: EmaJarKey`