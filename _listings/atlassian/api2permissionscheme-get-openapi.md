---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Jira Cloud API Get all permission schemes
  description: |-
    Returns all permission schemes.

    ### About permission schemes and grants

    A permission scheme is a collection of permission grants. A permission grant consists of a `holder` and a `permission`.

    #### Holder

    The `holder` object contains information about the user or group being granted the permission. For example, the _Administer projects_ permission is granted to a group named _Teams in space administrators_. In this case, the type is `"type": "group"`, and the parameter is the group name, `"parameter": "Teams in space administrators"`. The `holder` object is defined by the following properties:

    *   `type` Identifies the user or group (see the list of types below).
    *   `parameter` The value of this property depends on the `type`. For example, if the `type` is a group, then you need to specify the group name.

    The following `types` are available. The expected values for the `parameter` are given in parenthesis (some `types` may not have a `parameter`):

    *   `anyone` Grant for anonymous users.
    *   `applicationRole` Grant for users with access to the specified application (application name). See [Manage application access](https://confluence.atlassian.com/cloud/manage-application-access-744721629.html) for more information.
    *   `assignee` Grant for the user currently assigned to an issue.
    *   `group` Grant for the specified group (group name).
    *   `groupCustomField` Grant for a user in the group selected in the specified custom field (custom field ID).
    *   `projectLead` Grant for a project lead.
    *   `projectRole` Grant for the specified project role (project role ID).
    *   `reporter` Grant for the user who reported the issue.
    *   `sd.customer.portal.only` Jira Service Desk only. Grants customers permission to access the customer portal but not Jira. See [Customizing Jira Service Desk permissions](https://confluence.atlassian.com/x/24dKLg) for more information.
    *   `user` Grant for the specified user (user ID).
    *   `userCustomField` Grant for a user selected in the specified custom field (custom field ID).

    #### Permissions

    The [built-in Jira permissions](https://confluence.atlassian.com/x/yodKLg) are listed below. Apps can also define custom permissions. See the [project permission](https://developer.atlassian.com/cloud/jira/platform/modules/project-permission/) and [global permission](https://developer.atlassian.com/cloud/jira/platform/modules/global-permission/) module documentation for more information.

    **Project permissions**

    *   `ADMINISTER_PROJECTS`
    *   `BROWSE_PROJECTS`
    *   `MANAGE_SPRINTS_PERMISSION` (Jira Software only)
    *   `SERVICEDESK_AGENT` (Jira Service Desk only)
    *   `VIEW_DEV_TOOLS` (Jira Software only)
    *   `VIEW_READONLY_WORKFLOW`

    **Issue permissions**

    *   `ASSIGNABLE_USER`
    *   `ASSIGN_ISSUES`
    *   `CLOSE_ISSUES`
    *   `CREATE_ISSUES`
    *   `DELETE_ISSUES`
    *   `EDIT_ISSUES`
    *   `LINK_ISSUES`
    *   `MODIFY_REPORTER`
    *   `MOVE_ISSUES`
    *   `RESOLVE_ISSUES`
    *   `SCHEDULE_ISSUES`
    *   `SET_ISSUE_SECURITY`
    *   `TRANSITION_ISSUES`

    **Voters and watchers permissions**

    *   `MANAGE_WATCHERS`
    *   `VIEW_VOTERS_AND_WATCHERS`

    **Comments permissions**

    *   `ADD_COMMENTS`
    *   `DELETE_ALL_COMMENTS`
    *   `DELETE_OWN_COMMENTS`
    *   `EDIT_ALL_COMMENTS`
    *   `EDIT_OWN_COMMENTS`

    **Attachments permissions**

    *   `CREATE_ATTACHMENTS`
    *   `DELETE_ALL_ATTACHMENTS`
    *   `DELETE_OWN_ATTACHMENTS`

    **Time tracking permissions**

    *   `DELETE_ALL_WORKLOGS`
    *   `DELETE_OWN_WORKLOGS`
    *   `EDIT_ALL_WORKLOGS`
    *   `EDIT_OWN_WORKLOGS`
    *   `WORK_ON_ISSUES`

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira.
  termsOfService: http://atlassian.com/terms/
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/2/permissionscheme:
    get:
      summary: Get all permission schemes
      description: |-
        Returns all permission schemes.

        ### About permission schemes and grants

        A permission scheme is a collection of permission grants. A permission grant consists of a `holder` and a `permission`.

        #### Holder

        The `holder` object contains information about the user or group being granted the permission. For example, the _Administer projects_ permission is granted to a group named _Teams in space administrators_. In this case, the type is `"type": "group"`, and the parameter is the group name, `"parameter": "Teams in space administrators"`. The `holder` object is defined by the following properties:

        *   `type` Identifies the user or group (see the list of types below).
        *   `parameter` The value of this property depends on the `type`. For example, if the `type` is a group, then you need to specify the group name.

        The following `types` are available. The expected values for the `parameter` are given in parenthesis (some `types` may not have a `parameter`):

        *   `anyone` Grant for anonymous users.
        *   `applicationRole` Grant for users with access to the specified application (application name). See [Manage application access](https://confluence.atlassian.com/cloud/manage-application-access-744721629.html) for more information.
        *   `assignee` Grant for the user currently assigned to an issue.
        *   `group` Grant for the specified group (group name).
        *   `groupCustomField` Grant for a user in the group selected in the specified custom field (custom field ID).
        *   `projectLead` Grant for a project lead.
        *   `projectRole` Grant for the specified project role (project role ID).
        *   `reporter` Grant for the user who reported the issue.
        *   `sd.customer.portal.only` Jira Service Desk only. Grants customers permission to access the customer portal but not Jira. See [Customizing Jira Service Desk permissions](https://confluence.atlassian.com/x/24dKLg) for more information.
        *   `user` Grant for the specified user (user ID).
        *   `userCustomField` Grant for a user selected in the specified custom field (custom field ID).

        #### Permissions

        The [built-in Jira permissions](https://confluence.atlassian.com/x/yodKLg) are listed below. Apps can also define custom permissions. See the [project permission](https://developer.atlassian.com/cloud/jira/platform/modules/project-permission/) and [global permission](https://developer.atlassian.com/cloud/jira/platform/modules/global-permission/) module documentation for more information.

        **Project permissions**

        *   `ADMINISTER_PROJECTS`
        *   `BROWSE_PROJECTS`
        *   `MANAGE_SPRINTS_PERMISSION` (Jira Software only)
        *   `SERVICEDESK_AGENT` (Jira Service Desk only)
        *   `VIEW_DEV_TOOLS` (Jira Software only)
        *   `VIEW_READONLY_WORKFLOW`

        **Issue permissions**

        *   `ASSIGNABLE_USER`
        *   `ASSIGN_ISSUES`
        *   `CLOSE_ISSUES`
        *   `CREATE_ISSUES`
        *   `DELETE_ISSUES`
        *   `EDIT_ISSUES`
        *   `LINK_ISSUES`
        *   `MODIFY_REPORTER`
        *   `MOVE_ISSUES`
        *   `RESOLVE_ISSUES`
        *   `SCHEDULE_ISSUES`
        *   `SET_ISSUE_SECURITY`
        *   `TRANSITION_ISSUES`

        **Voters and watchers permissions**

        *   `MANAGE_WATCHERS`
        *   `VIEW_VOTERS_AND_WATCHERS`

        **Comments permissions**

        *   `ADD_COMMENTS`
        *   `DELETE_ALL_COMMENTS`
        *   `DELETE_OWN_COMMENTS`
        *   `EDIT_ALL_COMMENTS`
        *   `EDIT_OWN_COMMENTS`

        **Attachments permissions**

        *   `CREATE_ATTACHMENTS`
        *   `DELETE_ALL_ATTACHMENTS`
        *   `DELETE_OWN_ATTACHMENTS`

        **Time tracking permissions**

        *   `DELETE_ALL_WORKLOGS`
        *   `DELETE_OWN_WORKLOGS`
        *   `EDIT_ALL_WORKLOGS`
        *   `EDIT_OWN_WORKLOGS`
        *   `WORK_ON_ISSUES`

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira.
      operationId: com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.getAllPermissionSchemes_g
      x-api-path-slug: api2permissionscheme-get
      parameters:
      - in: query
        name: expand
        description: Use expand to include additional information in the response
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Schemes
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---