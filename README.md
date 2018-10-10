# L2L Framework
Documentation and Utilities related to the L2L Framework.
- [Scenario](scenario.md)
- [Workshop](workshop.md)

## L2L Infrastructure
### Gateway
- repository addr : <git@github.com:i-qiqi/l2l-gateway.git>

### Registry
- repository addr : <git@github.com:i-qiqi/l2l-registry.git>
- registry bug : the front end is not present after the backend has started up.
```bash
# adjust to proper node version
nvm use 8
# add node-sass
yarn
yarn add node-sass
yarn start
# Ctrl + c , re-run registry
./gradlew
```

## L2L Core Components
### Vessel enterprise
Note : suggest that we can refer to the implementation [`ttc-rb-english-campaign`](git@github.com:Activiti/ttc-rb-english-campaign.git)
- repository addr : <git@github.com:i-qiqi/l2l-vesslel-enterprise.git>

### VMC(Vessel-Manager-Coordinator)
Note : suggest that we can refer to the implementation [ttc-connectors-reword](git@github.com:Activiti/ttc-connectors-reward.git)
- repository addr : <git@github.com:i-qiqi/l2l-vmc.git>

## L2L Frontend
## Reference
- [Activiti7 Guide](https://activiti.gitbook.io/activiti-7-developers-guide/components-architecture/activiti-cloud-infrastructure/gateway)
-  [Cloud native in kubernetes workshop](https://github.com/Activiti/ttc-docs/blob/develop/workshop.md)
