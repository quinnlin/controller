# Changelog

## 0.2.1 (July 21, 2016)

- Fixed bug where controller did not send rule updates to sidecar in
  polling mode.

## 0.2.0 (July 20, 2016)

- The controller no longer generates Nginx config files in response to
  changes in the service instance pool. Instead, these 
  updates are passed on to the sidecar which in turn passes them onto the
  Lua code that now manages the upstreams.  This decoupling of
  configuration management from the controller provides the user with full
  control over the nginx configuration in each sidecar, allowing her to
  customize the configuration (e.g., add HTTPS certificates, custom
  modules, etc.).

- All environment variables pertaining to the controller are now prefixed
  with A8_.

- TENANT_ID is no longer needed nor accepted. Tenants are distinguished by
  unique authentication tokens that needs to be present in each request to
  the controller.

- Several bug fixes

## 0.1.0 (June 28, 2016)
- Initial release of the Amalgam8 Controller.
