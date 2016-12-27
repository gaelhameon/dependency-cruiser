# dependency-cruiser's json output format

A [json schema](../src/extract/jsonschema.json) describes the output format.
The schema is accurate and actual - each build unit tests assure the output
format adheres to the schema.

A sample output (for the popular [commander.js](https://github.com/tj/commander.js)
module):

```json
{
    "dependencies": [
        {
            "source": "commander/index.js",
            "dependencies": [
                {
                    "resolved": "child_process",
                    "coreModule": true,
                    "followable": false,
                    "couldNotResolve": false,
                    "dependencyTypes": [
                        "core"
                    ],
                    "module": "child_process",
                    "moduleSystem": "cjs",
                    "valid": true
                },
                {
                    "resolved": "events",
                    "coreModule": true,
                    "followable": false,
                    "couldNotResolve": false,
                    "dependencyTypes": [
                        "core"
                    ],
                    "module": "events",
                    "moduleSystem": "cjs",
                    "valid": true
                },
                {
                    "resolved": "fs",
                    "coreModule": true,
                    "followable": false,
                    "couldNotResolve": false,
                    "dependencyTypes": [
                        "core"
                    ],
                    "module": "fs",
                    "moduleSystem": "cjs",
                    "valid": true
                },
                {
                    "resolved": "graceful-readlink/index.js",
                    "coreModule": false,
                    "followable": true,
                    "couldNotResolve": false,
                    "dependencyTypes": [
                        "npm"
                    ],
                    "module": "graceful-readlink",
                    "moduleSystem": "cjs",
                    "valid": true
                },
                {
                    "resolved": "path",
                    "coreModule": true,
                    "followable": false,
                    "couldNotResolve": false,
                    "dependencyTypes": [
                        "core"
                    ],
                    "module": "path",
                    "moduleSystem": "cjs",
                    "valid": true
                }
            ]
        },
        {
            "source": "child_process",
            "followable": false,
            "coreModule": true,
            "couldNotResolve": false,
            "dependencyTypes": [
                "npm"
            ],
            "dependencies": []
        },
        {
            "source": "events",
            "followable": false,
            "coreModule": true,
            "couldNotResolve": false,
            "dependencyTypes": [
                "core"
            ],
            "dependencies": []
        },
        {
            "source": "fs",
            "followable": false,
            "coreModule": true,
            "couldNotResolve": false,
            "dependencyTypes": [
                "core"
            ],
            "dependencies": []
        },
        {
            "source": "path",
            "followable": false,
            "coreModule": true,
            "couldNotResolve": false,
            "dependencyTypes": [
                "core"
            ],
            "dependencies": []
        },
        {
            "source": "graceful-readlink/index.js",
            "dependencies": [
                {
                    "resolved": "fs",
                    "coreModule": true,
                    "followable": false,
                    "couldNotResolve": false,
                    "dependencyTypes": [
                        "core"
                    ],
                    "module": "fs",
                    "moduleSystem": "cjs",
                    "valid": true
                }
            ]
        }
    ],
    "summary" {
        "violations": [],
        "error": 0,
        "warn": 0,
        "info": 0,
        "totalCruised": 6,
        "usedOptions": {
            "outputType": "json"
        }
    }
}
```