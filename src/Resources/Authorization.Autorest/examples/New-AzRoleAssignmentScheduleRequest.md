### Example 1: Create a new role assignment schedule request as Admin
```powershell
PS C:\> $guid = "12f8978c-5d8d-4fbf-b4b6-2f43eeb43eca"
PS C:\> $startTime = Get-Date -Format o 
PS C:\> $scope = "/subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d/"
PS C:\> New-AzRoleAssignmentScheduleRequest -Name $guid -Scope $scope -ExpirationDuration PT1H -ExpirationType AfterDuration -PrincipalId 5a4bdd72-ab3e-4d8e-ab0f-8dd8917481a2 -RequestType AdminAssign -RoleDefinitionId subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d/providers/Microsoft.Authorization/roleDefinitions/acdd72a7-3385-48ef-bd42-f606fba81ae7 -ScheduleInfoStartDateTime $startTime

Name                                 Type                                                    Scope                                               RoleDefinitionId
----                                 ----                                                    -----                                               ----------------                                                                 
12f8978c-5d8d-4fbf-b4b6-2f43eeb43eca Microsoft.Authorization/roleAssignmentScheduleRequests /subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d /subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d/providers/Microsoft.Authori… 
```

Creates a request to provision an active assignment of `roleDefinition` on the `scope` for the specified `principal`

### Example 2: Remove a role assignment schedule request as Admin
```powershell
PS C:\> $guid = "13f8978c-5d8d-4fbf-b4b6-2f43eeb43eca"
PS C:\> $startTime = Get-Date -Format o 
PS C:\> $scope = "/subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d/"
PS C:\> New-AzRoleAssignmentScheduleRequest -Name $guid -Scope $scope -ExpirationDuration PT1H -ExpirationType AfterDuration -PrincipalId 5a4bdd72-ab3e-4d8e-ab0f-8dd8917481a2 -RequestType AdminRemove -RoleDefinitionId subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d/providers/Microsoft.Authorization/roleDefinitions/acdd72a7-3385-48ef-bd42-f606fba81ae7 -ScheduleInfoStartDateTime $startTime

Name                                 Type                                                    Scope                                               RoleDefinitionId
----                                 ----                                                    -----                                               ----------------                                                                 
13f8978c-5d8d-4fbf-b4b6-2f43eeb43eca Microsoft.Authorization/roleAssignmentScheduleRequests /subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d /subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d/providers/Microsoft.Authori… 
```

Creates a request to remove an active assignment of `roleDefinition` on the `scope` for the specified `principal`

### Example 3: Activate a new role assignment schedule request as user
```powershell
PS C:\> $guid = "12f8978c-5d8d-4fbf-b4b6-2f43eeb43eca"
PS C:\> $startTime = Get-Date -Format o 
PS C:\> $scope = "/subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d/"
PS C:\> New-AzRoleAssignmentScheduleRequest -Name $guid -Scope $scope -ExpirationDuration PT1H -ExpirationType AfterDuration -PrincipalId 5a4bdd72-ab3e-4d8e-ab0f-8dd8917481a2 -RequestType SelfActivate -RoleDefinitionId subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d/providers/Microsoft.Authorization/roleDefinitions/acdd72a7-3385-48ef-bd42-f606fba81ae7 -ScheduleInfoStartDateTime $startTime

Name                                 Type                                                    Scope                                               RoleDefinitionId
----                                 ----                                                    -----                                               ----------------                                                                 
12f8978c-5d8d-4fbf-b4b6-2f43eeb43eca Microsoft.Authorization/roleAssignmentScheduleRequests /subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d /subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d/providers/Microsoft.Authori… 
```

Creates a request to activate an eligible assignment of `roleDefinition` on the `scope` for the specified `principal`

### Example 4: Deactivate a role assignment schedule request as user
```powershell
PS C:\> $guid = "12f8978c-5d8d-4fbf-b4b6-2f43eeb43eca"
PS C:\> $startTime = Get-Date -Format o 
PS C:\> $scope = "/subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d/"
PS C:\> New-AzRoleAssignmentScheduleRequest -Name $guid -Scope $scope -ExpirationDuration PT1H -ExpirationType AfterDuration -PrincipalId 5a4bdd72-ab3e-4d8e-ab0f-8dd8917481a2 -RequestType SelfDeactivate -RoleDefinitionId subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d/providers/Microsoft.Authorization/roleDefinitions/acdd72a7-3385-48ef-bd42-f606fba81ae7 -ScheduleInfoStartDateTime $startTime

Name                                 Type                                                    Scope                                               RoleDefinitionId
----                                 ----                                                    -----                                               ----------------                                                                 
12f8978c-5d8d-4fbf-b4b6-2f43eeb43eca Microsoft.Authorization/roleAssignmentScheduleRequests /subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d /subscriptions/38ab2ccc-3747-4567-b36b-9478f5602f0d/providers/Microsoft.Authori… 
```

Creates a request to deactivate an eligible assignment of `roleDefinition` on the `scope` for the specified `principal`

