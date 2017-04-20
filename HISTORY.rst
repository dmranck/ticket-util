Release History
---------------

1.1.0 (04-18-2017)
++++++++++++++++++

* JIRA, Bugzilla, RT, Redmine

  - Added get_ticket_url() method to return ticket url for Ticket object.
  - Added get_ticket_id() method to return ticket id for Ticket object.
  - Added _verify_project() and _verify_ticket_id() methods to all tools.
    These methods are called when a new Ticket object is created to verify
    that the project and optional ticket_id parameters are valid.
  - Created TicketException class, which is raised if the url passed in
    during creation of a Ticket object can not be accessed. This exception
    is also raised if project or ticket_id can not be verified.
  - The environment variable TICKETUTIL_DEBUG has been replaced with
    TICKETUTIL_LOG_LEVEL, with a default value of 'INFO'. This allows you to
    turn on debug logging by setting this variable to 'DEBUG' and effectively
    turn off logging by setting it to 'CRITICAL'.

* JIRA

  - Modified _get_status_id() in jira.py to return the status_id
    corresponding to the state you are transitioning to, instead of the
    status_id corresponding to the transition itself.

* Bugzilla

  - Added add_attachment() method.
  - Added support for api_key authentication.
  - Added support for adding groups to ticket in create() and edit().

* RT

  - Added add_attachment() method.

* Redmine

  - Added add_attachment() method.

1.0.6 (01-20-2017)
++++++++++++++++++
- Trying to fix more PyPI issues.

1.0.5 (01-20-2017)
++++++++++++++++++
- Fixing README on PyPI.

1.0.4 (01-20-2017)
++++++++++++++++++
- Updated JIRA example and docstring to clarify that 'type' (and not
  'issuetype') is a supported create() and edit() field. No code changes.

1.0.3 (01-19-2017)
++++++++++++++++++
- First publish to PyPI!
