TravisTemplateForMono
=====================

## Changes from Original ```NuGet.targets```


```
    <PropertyGroup Condition=" '$(OS)' != 'Windows_NT'">
        <!-- We need to launch nuget.exe with the mono command if we're not on windows -->
        <NuGetToolsPath>$(SolutionDir).nuget</NuGetToolsPath>
        <!-- Fixed for Travis CI because xbuild fails to find packages.config -->
        <PackagesConfig>packages.config</PackagesConfig>
        <!-- If you want to use a project config file, please use the following instead -->
        <!-- <PackagesConfig>$(PackagesProjectConfig)</PackagesConfig> -->
    </PropertyGroup>
```

