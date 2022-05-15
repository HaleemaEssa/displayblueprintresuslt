- tar czf blue_10_1.tar.gz blueprint
- cfy blueprints upload blue_10_1.tar.gz -n blueprint.yaml -b myblueprint
Uploading blueprint blue_10_1.tar.gz...
 blue_10_1.tar.gz |####################################################| 100.0%
Blueprint `myblueprint` upload started.
2022-05-15 21:36:15.597  CFY <None> Starting 'upload_blueprint' workflow execution
2022-05-15 21:36:15.663  LOG <None> INFO: Blueprint archive uploaded. Extracting...
2022-05-15 21:36:15.752  LOG <None> INFO: Blueprint archive extracted. Parsing...
2022-05-15 21:36:17.590  LOG <None> INFO: Blueprint parsed. Updating DB with blueprint plan.
2022-05-15 21:36:17.610  LOG <None> WARNING: Node 'App-RPi' contains multiple relationships with the same target. Only the last of these will have its interface operations executed.
2022-05-15 21:36:17.634  LOG <None> WARNING: Node 'finalBlock' contains multiple relationships with the same target. Only the last of these will have its interface operations executed.
2022-05-15 21:36:17.773  CFY <None> 'upload_blueprint' workflow execution succeeded
Blueprint uploaded. The blueprint's id is myblueprint
- cfy deployments create -b myblueprint
Creating new deployment from blueprint myblueprint...
Deployment `myblueprint` created. The deployment's id is myblueprint
- cfy executions start install -d myblueprint
Executing workflow `install` on deployment `myblueprint` [timeout=900 seconds]
2022-05-15 21:38:41.947  CFY <myblueprint> Starting 'install' workflow execution
2022-05-15 21:38:42.145  CFY <myblueprint> Subgraph started 'install_RPi_lvla36'
2022-05-15 21:38:42.168  CFY <myblueprint> Subgraph started 'install_pc_nj07xj'
2022-05-15 21:38:42.246  CFY <myblueprint> [RPi_lvla36] Validating node instance before creation: nothing to do
2022-05-15 21:38:42.282  CFY <myblueprint> [RPi_lvla36] Precreating node instance: nothing to do
2022-05-15 21:38:42.315  CFY <myblueprint> [pc_nj07xj] Validating node instance before creation: nothing to do
2022-05-15 21:38:42.315  CFY <myblueprint> [RPi_lvla36] Creating node instance: nothing to do
2022-05-15 21:38:42.340  CFY <myblueprint> [RPi_lvla36] Configuring node instance: nothing to do
2022-05-15 21:38:42.345  CFY <myblueprint> [pc_nj07xj] Precreating node instance: nothing to do
2022-05-15 21:38:42.365  CFY <myblueprint> [RPi_lvla36] Starting node instance: nothing to do
2022-05-15 21:38:42.375  CFY <myblueprint> [pc_nj07xj] Creating node instance: nothing to do
2022-05-15 21:38:42.395  CFY <myblueprint> [RPi_lvla36] Poststarting node instance: nothing to do
2022-05-15 21:38:42.405  CFY <myblueprint> [pc_nj07xj] Configuring node instance: nothing to do
2022-05-15 21:38:42.433  CFY <myblueprint> [RPi_lvla36] Node instance started
2022-05-15 21:38:42.437  CFY <myblueprint> [pc_nj07xj] Starting node instance: nothing to do
2022-05-15 21:38:42.466  CFY <myblueprint> [pc_nj07xj] Poststarting node instance: nothing to do
2022-05-15 21:38:42.476  CFY <myblueprint> Subgraph succeeded 'install_RPi_lvla36'
2022-05-15 21:38:42.503  CFY <myblueprint> Subgraph started 'install_container-RPi_min16e'
2022-05-15 21:38:42.537  CFY <myblueprint> [pc_nj07xj] Node instance started
2022-05-15 21:38:42.542  CFY <myblueprint> [container-RPi_min16e] Node instance started (nothing to do)
2022-05-15 21:38:42.589  CFY <myblueprint> Subgraph succeeded 'install_container-RPi_min16e'
2022-05-15 21:38:42.615  CFY <myblueprint> Subgraph succeeded 'install_pc_nj07xj'
2022-05-15 21:38:42.639  CFY <myblueprint> Subgraph started 'install_container1_96gkqd'
2022-05-15 21:38:42.666  CFY <myblueprint> Subgraph started 'install_App-RPi_t40q6g'
2022-05-15 21:38:42.669  CFY <myblueprint> [container1_96gkqd] Node instance started (nothing to do)
2022-05-15 21:38:42.703  CFY <myblueprint> [App-RPi_t40q6g] Node instance started (nothing to do)
2022-05-15 21:38:42.718  CFY <myblueprint> Subgraph succeeded 'install_container1_96gkqd'
2022-05-15 21:38:42.756  CFY <myblueprint> Subgraph succeeded 'install_App-RPi_t40q6g'
2022-05-15 21:38:42.780  CFY <myblueprint> Subgraph started 'install_finalBlock_rw4sk7'
2022-05-15 21:38:42.804  CFY <myblueprint> [finalBlock_rw4sk7] Node instance started (nothing to do)
2022-05-15 21:38:42.839  CFY <myblueprint> Subgraph succeeded 'install_finalBlock_rw4sk7'
2022-05-15 21:38:42.862  CFY <myblueprint> 'install' workflow execution succeeded
Finished executing workflow install on deployment myblueprint
