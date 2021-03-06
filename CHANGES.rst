Changes
=======

Version 0.7.0 (2020-10-20)
--------------------------

- Adds possibility to restart workflows.
- Adds exposure of workflow engines logs.
- Adds possibility to pass workflow operational options.
- Adds progress report information on workflow list response.
- Adds code mount on dev mode in workflow engines and job controller.
- Adds preview flag to file download endpoint.
- Fixes deletion of workflows in queued state.
- Fixes CVMFS availability for interactive sessions.
- Fixes jobs status update.
- Fixes response on close interactive session action.
- Changes runtime component creation to use centrally configured namespace from REANA-Commons.
- Changes workflow engine pod labelling for better traceability.
- Changes logs endpoint to provide richer information.
- Changes git clone depth when retrieving GitLab projects.
- Changes REANA submodule installation in editable mode for live code updates for developers.
- Changes base image to use Python 3.8.
- Changes code formatting to respect ``black`` coding style.
- Changes documentation to single-page layout.

Version 0.6.1 (2020-05-25)
--------------------------

- Upgrades REANA-Commons package using latest Kubernetes client version.

Version 0.6.0 (2019-12-20)
--------------------------

- Modifies the batch workflow run creation, including an instance of
  REANA-Job-Controller running alongside with the workflow engine (sidecar
  pattern). Only DB and workflow worksapce are mounted.
- Refactors volume mounts using `reana-commons` base.
- Provides user secrets to the job controller.
- Extends workflow APIs for GitLab integration.
- Allows stream file uploads.


Version 0.5.0 (2019-04-23)
--------------------------

- Adds support to create interactive sessions so the workspace can be explored
  and modified through a Jupyter notebook.
- Creates workflow engine instances on demand for each user and makes CVMFS
  available inside of them.
- Adds new endpoint to compare two workflows. The output is a ``git`` like
  diff which can be configured to show differences at metadata level,
  workspace level or both.
- Adds new endpoint to delete workflows including the stopped ones.
- Adds new endpoints to delete and move files whithin the workspace.
  The deletion can be also done recursively with a wildcard.
- Adds new endpoint which returns workflow parameters.
- Adds new endpoint to query the disk usage of a given workspace.
- Makes docker image slimmer by using ``python:3.6-slim``.
- Centralises log level and log format configuration.

Version 0.4.0 (2018-11-06)
--------------------------

- Improves AMQP re-connection handling. Switches from ``pika`` to ``kombu``.
- Improves REST API documentation rendering.
- Changes license to MIT.

Version 0.3.2 (2018-09-25)
--------------------------

- Modifies job input identification process for caching purposes, adding compatibility
  with CephFS storage volumes.

Version 0.3.1 (2018-09-07)
--------------------------

- Harmonises date and time outputs amongst various REST API endpoints.
- Separates workflow parameters and engine parameters when running Serial
  workflows.
- Pins REANA-Commons and REANA-DB dependencies.

Version 0.3.0 (2018-08-10)
--------------------------

- Adds support for
  `Serial workflows <http://reana-workflow-engine-serial.readthedocs.io/en/latest/>`_.
- Tracks progress of workflow runs.
- Adds uwsgi for production deployments.
- Allows downloading of any file from a workflow workspace.

Version 0.2.0 (2018-04-19)
--------------------------

- Adds support for Common Workflow Language workflows.
- Adds support for specifying workflow names in REST API requests.
- Adds sequential incrementing of workflow run numbers.
- Adds support for nested inputs and runtime code directory uploads.
- Improves error messages and information.
- Prevents multiple starts of the same workflow.

Version 0.1.0 (2018-01-30)
--------------------------

- Initial public release.

.. admonition:: Please beware

   Please note that REANA is in an early alpha stage of its development. The
   developer preview releases are meant for early adopters and testers. Please
   don't rely on released versions for any production purposes yet.
