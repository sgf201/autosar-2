# Watch Dog

## WdgM
Configure the Alive Supervision

### Supervised Entity
**Deadline Supervision doesn't need init since it contain start point**
1. Add Supervised Entity (SE_XXX)
1. Add Checkpoint
    1. CP_XXX_AS0
    1. CP_XXX_ILS_0
    1. CP_XXX_ILS_1
    1. CP_XXX_ILS_2

### Mode
1. Add WdgMMode
1. Add following itmes by right click
    1. Alive Supervision
    1. Local Status Params
    1. Trigger
1. In *Alive Supervision*, set numbers and add Checkpoint Ref
1. In *Local Status Params*, register SE_XXX in *Local Status Supervised Entity Ref*
1. In *Trigger*, 

#### Local Status Params


## Go to SWC to be supervised
1. Go to Ports
1. Add WdgM_API, WdgM_AliveSupervision as a *Client Interface*
1. Rename WdgM_AliveSupervision to SE_XXX
1. Rename WdgM_API to WdgM_API_R
1. Go to Runnables > Operation/Mode/Trigger Access
1. Add Synchronous Server Call Points
    1. CheckpointReached
    1. SetMode
    1. GetFirstExpiredSEID
    1. GetGlobalStatus


## Go to EcucValueCollection
1. Connect WdgM_API_P (to WdgM_API_R)
1. Connect alive_SE_XXX