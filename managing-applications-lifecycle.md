# Managing the Applications Lifecycle

## Deploy Applications

### Configure Application Settings After Deployment

What is the most **correct and
recommended way** to make sure the application is using the
Production-like data in the Quality environment?
**After** deploying the application to Quality, access Service Center in Quality and change the **Effective URL** of the integration to the new URL.

### Applying Configurations in Service Center

Operation Settings
* Stored in database.
* When save changes to operation settings, changes are effective immediately after clearing the cache for the setting (e.g. the schedule of a timer).

Runtime Settings
* When **apply** change runtime settings for **application**, module or extension, cause reload of affected modules (e.g. Effective URL).
* When **save** change runtime settings for **environment**, changes are saved first. **Republish** or **redeploy** module will apply changes.
* When **save and apply settings to the factory**, cause reload of all modules.

Compile-time Settings
* After changing a compile-time setting, need to **republish** modules so that new configuration values are taken when compiling.

Reference
https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Deploy_Applications/Configure_Application_Settings_After_Deployment/Applying_Configurations_in_Service_Center#settings-reference

## Manage IT Users

* Roles assigned to a user for teams **override the default role** of the user.
* Roles assigned to a user on specific applications **override the default role** of the user and also **any role assigned through teams**.

### Permission levels for an environment

| Permision | Default Role | Team | Application |
| ----------- | ----------- | ----------- | ----------- |
| Full Control | User can manage **environment settings**. | NA | NA |
| Change and Deploy Applications | User can see **environment’s applications** in Service Studio, LifeTime and Service Center. User can change settings of **environment's applications**. | User can see **team’s applications** in Service Studio, LifeTime and Service Center. User can change settings of **team's applications**. | User can see **application** in Service Studio, LifeTime and Service Center. User can change settings of **application**. |
| Open and Debug Applications | User can open and debug **modules of environment's applications** using `Ctrl-O`. | User an open and debug **modules of team's applications** using `Ctrl-O`. | User can open and debug **modules of application** using `Ctrl-O`. |
| Monitor and Add Dependencies | User can add dependencies to the public elements of  **environment’s applications**. User can monitor  **environment’s applications** and **environment’s performance**. | User can add dependencies to the public elements of **team’s applications**. User can monitor **team’s applications**. | User can add dependencies to the public elements of **application**. User can monitor **application**. |
| List Applications | User can see **environment's applications** in LifeTime and Service Center. | User can see **teams's applications** in LifeTime and Service Center. | User can see **application** in LifeTime and Service Center. |
| Access | User can login to **environment**. | Same as **No Access**. | Same as **No Access**. |
| No Access | User cannot login to **environment**. | User cannot see **team’s applications** in LifeTime, Service Center or Service Studio. | User cannot see **application** in LifeTime, Service Center or Service Studio. |

### Specific permissions for an environment

| Permision | Default Role | Team | Application |
| ----------- | ----------- | ----------- | ----------- |
| Create Applications | User can create new applications in **environment** in Service Studio and Service Center. User can create new applications in **any team** in LifeTime. | User can create new applications in **team** in LifeTime. | NA |
| Add System Dependencies | User can add new dependencies to public elements of System module. | NA | NA |

### Infrastructure-wide permissions

| Permision | Default Role | Team | Application |
| ----------- | ----------- | ----------- | ----------- |
| Manage Users and Roles (Setting this ON also sets "Manage Teams and Application Roles" ON) | User can add/edit/remove IT users, roles and teams. User can turn on/off features in Technical Preview. | NA | NA |
| Manage Teams and Application Roles | User can add/remove IT users from **environment's team**. User can grant/revoke roles to IT users for **environment's applications**. User can edit **environment's teams** and access the audit logs. | User can add/remove IT users from **team**. User can grant/revoke roles to IT users for **team's applications**. User can edit **team** and access the **team's** audit logs. | User can grant/revoke roles to IT users for **application**. User can access  **application's** audit logs. |

### Allow Integrations With External Databases

- Create role with permission **Change and Deploy Applications**.
- Service Center > Administration > Database Connections.
- Grant **Publish** to role.
- To allow access to data on external database through extension, grant **Full Control**.