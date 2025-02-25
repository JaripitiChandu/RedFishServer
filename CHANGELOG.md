# Change Log

## [1.2.9] - 2024-05-03
- Added basic handling for multipart requests

## [1.2.8] - 2024-04-12
- Updated integrated mockup to version 2023.3 of public-rackmount1

## [1.2.7] - 2024-04-05
- Minor updates to improve Docker usage on different platform architectures

## [1.2.6] - 2024-03-22
- Updated Docker compose file to automatically generate TLS certificate and key

## [1.2.5] - 2024-03-01
- Added sample Docker compose file
- Migrated away from deprecated 'ssl.wrap_socket' method

## [1.2.4] - 2023-12-01
- Added better handling of resource creation operations to not rely on a resource identifier to be given
- Added the  response header when a new session is created

## [1.2.3] - 2023-05-15
- Fixes to SSDP listener to bind to all interfaces as well as enable listening on the loopback address

## [1.2.2] - 2023-02-24
- Updated bundled mockup to match 2022.3 release of public-rackmount1

## [1.2.1] - 2023-01-20
- Added support for binary files in a mockup

## [1.2.0] - 2023-01-13
- Import Mapping from collections.abc to support Python 3.10

## [1.1.9] - 2022-08-12
- Added SIGTERM handler to close the server

## [1.1.8] - 2022-06-03
- Added baseline support for the '$expand' query parameter

## [1.1.7] - 2021-07-02
- Added Content-Length header to responses for statically built /redfish

## [1.1.6] - 2021-06-18
- Added Content-Length header to responses

## [1.1.5] - 2021-02-15
- Made changes to hide `HttpHeaders` contents in event subscriptions

## [1.1.4] - 2020-11-13
- Added built-in "public-rackmount1" mockup

## [1.1.2] - 2020-10-30
- Made enhancement to collection management to fill in `Id` and `@odata.id` properly

## [1.1.1] - 2020-10-19
- Added Dockerfile to run the server as a Docker container
- Added expand support for resource collections

## [1.1.0] - 2020-05-09
- Added ability to POST to actions shown in the mockups so that a 2xx code is returned

## [1.0.9] - 2020-03-21
- Made corrections to the spelling of SSDP in the code

## [1.0.8] - 2019-03-26
- Fixed some issues with command line argument handling
- Fixed SSDP functionality
- Fixed issues with pathing on Windows

## [1.0.7] - 2019-02-08
- Fixed handling of PATCH/POST/PUT requests that do not contain a JSON body
- Added support for the SubmitTestMetricReport action

## [1.0.6] - 2018-10-12
- Added SSDP support within the service
- Added support for $top and $skip

## [1.0.5] - 2018-09-07
- Added Transfer-Encoding to the list of HTTP headers to not use

## [1.0.4] - 2018-07-16
- Fixed behavior of how the URIs are managed when issuing DELETE to members of a collection
- Added Location header in the service response when creating new resources

## [1.0.3] - 2018-05-25
- Added logic to remove the @Redfish.Copyright statement from payloads

## [1.0.2] - 2018-05-11
- Corrected Submit Test Event Action; it now verifies all required parameters are given, and the format of the Event it sends matches the Event schema

## [1.0.1] - 2018-04-13
- Made fixes for how POST and DELETE are handled with the Event Destination Collection
- Made fixes to the Submit Test Event action

## [1.0.0] - 2018-02-02
- Added support for HTTPS
- Added support for using "short" mockups (ones without the /redfish/v1 resource)
- Added support for submitting test events
- Added support for PATCH and PUT

## [0.9.7] - 2017-03-10
- Added support to delay time from json for GET and HEAD API  
    - "-T" option to include delay in time. If option not specified, there is no delay in response. Checks for time.json.
    - "-t <time_in_seconds>" to specify default time if time.json is not present.
- Added Response Header support for GETs: 
    - Checks for headers.json and includes required headers from it.
    - Certain headers like ("Connection", "Keep-Alive", "Content-Length") are not included in GET request.
- Added Support for HEAD Method
    - Checks for headers.json and includes required headers from it.
- Changed TestETag option to "-E" from "-T" 

## [0.9.3] - 2016-12-05
- -t <responseTime> option to specify a response delay for responses--to simulate a real system better
- fixed bug where GET /redfish/v1/$metadata was not being returned

## [0.9.2] - 2016-09-07
- added flush to server prints so that buffered stdout on cygwin would work
- added -T option to enable returning fake etags on certain APIs -instead of always doing it
- added -D <dir>  option  where <dir> is the abs or relative path to the mockup.  if no -D option, then CWD is assumed

## [0.9.1] - 2016-09-06
- Initial Public Release
