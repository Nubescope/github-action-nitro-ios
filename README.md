<!-- action-docs-description -->
### Description

A Gihub Action for building React Native apps with Nitro
<!-- action-docs-description -->

<!-- action-docs-inputs -->
### Inputs

| parameter | description | required | default |
| --- | --- | --- | --- |
| root-directory | The directory within your project, in which your code is located. Leave this field empty if your code is not located in a subdirectory" | `false` | . |
| scheme | The name of the iOS scheme | `false` |  |
| xcconfig-path | Path to a custom xcconfig file. The path relative to project root directory where the custom `.xcconfig` file is located | `false` |  |
| version-name | The version name for the app | `false` |  |
| version-code | The version code for the app | `false` |  |
| disable-version-name-from-package-json | Disable automatic version name configuration. By default will get the 'version' field from package.json and set the version name. Available Options: (`yes` / `no`) | `false` |  |
| disable-version-code-auto-generation | Disable automatic version code generation. By default will generate a timestamp based number and set the version code. Available Options: (`yes` / `no`) | `false` |  |
| certificate-url | Certificate url. The url to download and install the certificate | `false` |  |
| certificate-base64 | Certificate base64. The certificate base64 string enconded. | `false` |  |
| certificate-passphrase | Certificate passphrase | `false` |  |
| codesigning-identity | Codesigning identity | `false` |  |
| provisioning-profile-urls | Provisioning profile urls. A string containing a '|' separated values where provisioning profiles are located (e.g. `url1|url2``) | `false` |  |
| provisioning-profiles-base64 | Provisioning profiles in base64 format. A string containing a '|' separated values with provisioning profiles base64 encoded (e.g. `bXktcHJvdmlzaW9uaW5nLXByb2ZpbGUtY29udGVudC0x|bXktcHJvdmlzaW9uaW5nLXByb2ZpbGUtY29udGVudC0y`) | `false` |  |
| provisioning-profile-specifier | Provisioning profile specifier. The name of the provisioning profile when using a single one | `false` |  |
| team-id | Team ID. Specify the Team ID you want to use for the Apple Developer Portal | `false` |  |
| export-method | Export Method. The export method used to generate the IPA. Available Options: (`ad-hoc` / `app-store`) | `false` | ad-hoc |
| cache-provider | Cache provider where cache artifacts will be persisted. Available Options: (`fs`: File system / `github`: Uses Github cache action / `s3`: Amazon - Simple Storage Service) | `false` | s3 |
| disable-cache | When setting this option to `yes` build cache optimizations won't be performed.  Available Options: (`yes` / `no`) | `false` |  |
| cache-env-var-lookup-keys | List of env var keys for lookup to determine cache fingerprint. A list of `\|` separated values with env variable keys to lookup to determine whether the build should be cached or not | `false` |  |
| cache-file-lookup-paths | List of files for lookup to determine cache fingerprint. A list of `\|` separated value paths (relative to the root of the repo or absolute) to lookup in order to determine whether the build should be cached or not | `false` |  |
| disable-metro-cache | Setting this field to yes will disable the React Native Metro cache feature | `false` |  |
| pre-install-command | Run command prior to install project dependencies (e.g. `rm -rf ./some-folder`) | `false` |  |
| pre-build-command | Run command prior to start building the app (e.g. `yarn tsc && yarn test`) | `false` |  |
| post-build-command | Run command once build successfully finished (e.g. `yarn publish`) | `false` |  |
| output-directory | The path to the directory where to place all of Nitro's output files | `false` |  |
| entry-file | The entry file for bundle generation | `false` |  |
| detox-configuration | Select a device configuration from your defined configurations | `false` |  |
| debug | Enable verbose logs. Available Options: (`yes` / `no`) | `false` |  |
| fail-safe | Runing the app in this mode allows you to prevent the build to fail but you can check the status in further steps | `false` |  |
<!-- action-docs-inputs -->

<!-- action-docs-outputs -->
### Outputs

| parameter | description |
| --- | --- |
| nitro-build-status | The status of the latest build (success / failure) |
| nitro-output-dir | The path to the directory where to place all of Nitro's output files |
| nitro-logs-path | The full path to access the build log |
| nitro-summary-path | The full path to access the build summary report |
| nitro-app-path | The full path to access the iOS package (.app or .ipa) |
<!-- action-docs-outputs -->

<!-- action-docs-runs -->
### Runs

This action is a `composite` action.
<!-- action-docs-runs -->
