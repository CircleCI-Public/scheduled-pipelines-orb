# CircleCI Scheduled Pipelines Orb

[![CircleCI Build Status](https://circleci.com/gh/CircleCI-Public/scheduled-piplines.svg?style=shield "CircleCI Build Status")](https://circleci.com/gh/CircleCI-Public/scheduled-piplines) [![CircleCI Orb Version](https://badges.circleci.com/orbs/CircleCI-Public/scheduled-piplines.svg)](https://circleci.com/orbs/registry/orb/CircleCI-Public/scheduled-piplines) [![GitHub License](https://img.shields.io/badge/license-MIT-lightgrey.svg)](https://raw.githubusercontent.com/CircleCI-Public/scheduled-piplines/master/LICENSE) [![CircleCI Community](https://img.shields.io/badge/community-CircleCI%20Discuss-343434.svg)](https://discuss.circleci.com/c/ecosystem/orbs)

A CircleCI orb for updating pipeline schedules.

---

## Valid Schedule JSON Example

The file needs to contain a `json` object with an array of `schedules`. Each element in the `schedules` array is a valid payload for a `POST` request to the CircleCI Schedules API. You can find more details about the [schema here](https://circleci.com/docs/api/v2/index.html#operation/createSchedule).

Here's an example:

```json
{
    "schedules": [{
        "name": "string",
        "timetable": {
            "per-hour": 0,
            "hours-of-day": [
            0
            ],
            "days-of-week": [
            "TUE"
            ],
            "days-of-month": [
            0
            ],
            "months": [
            "MAR"
            ]
        },
        "attribution-actor": "current",
        "parameters": {
            "deploy_prod": true,
            "branch": "feature/design-new-api"
        },
        "description": "string"
        }
    ]
}
```

*NOTE:* In `timetable`, `days-of-week` and `days-of-month` are mutually exclusive and cannot be used together.

## Resources

[CircleCI Orb Registry Page](https://circleci.com/orbs/registry/orb/CircleCI-Public/scheduled-piplines) - The official registry page of this orb for all versions, executors, commands, and jobs described.

[CircleCI Orb Docs](https://circleci.com/docs/2.0/orb-intro/#section=configuration) - Docs for using, creating, and publishing CircleCI Orbs.

### How to Contribute

We welcome [issues](https://github.com/CircleCI-Public/scheduled-piplines/issues) to and [pull requests](https://github.com/CircleCI-Public/scheduled-piplines/pulls) against this repository!
