# Microsoft Service Monitor

**ServiceMonitor** is a Windows executable designed to be used as the entrypoint
process when running a service inside a Windows Server container.

ServiceMonitor will start and monitor windows services running inside a container. 
It monitors the status of your service and will exit when the service state 
changes from `SERVICE_RUNNING` to either one of `SERVICE_STOPPED`, 
`SERVICE_STOP_PENDING`, `SERVICE_PAUSED` or `SERVICE_PAUSE_PENDING`.

## Build

```
.\build.cmd
```

## Usage

```
.\ServiceMonitor.exe ServiceName
```

## Docker

Add ServiceMonitor.exe as the main entry point and specify the name of the service to monitor

```docker
ENTRYPOINT ["ServiceMonitor.exe", "MyServiceToMonitor"]
```

## Contributing

This project welcomes contributions and suggestions.  Most contributions require
you to agree to a Contributor License Agreement (CLA) declaring that you have
the right to, and actually do, grant us the rights to use your contribution. For
details, visit https://cla.microsoft.com.

When you submit a pull request, a CLA-bot will automatically determine whether
you need to provide a CLA and decorate the PR appropriately (e.g., label,
comment). Simply follow the instructions provided by the bot. You will only need
to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/)
or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any
additional questions or comments.


