# TLS

e.g. `cldr_tls_provider=opensslca`.

Layer host groups:
- `tls_certificates`
- `tls_servers`

Layer group vars:
- `cldr_tls_base_path`
- `cldr_tls_key_password`
- `cldr_tls_truststore_password`
- `cldr_tls_keytool_path`
- `cldr_tls_openssl_path`
- `cldr_tls_key_path_plaintext_generic`
- `cldr_tls_keystore_path_generic`
- `cldr_tls_truststore_path`
- `cldr_tls_key_path_generic`
- `cldr_tls_uber_truststore_path `
- `cldr_tls_ca_chain_path`

Layer host vars:
- `cldr_tls_fqdn` (defaults to inventory host)
- `cldr_tls_local_accounts` (defaults to cluster accounts)
- `cldr_tls_keystore_alias` (defaults to inventory host)
- `cldr_tls_user_owner`
- `cldr_tls_group_owner`
- `cldr_tls_san`
- `cldr_tls_certificate_path`
- `cldr_tls_csr_config_path`
- `cldr_tls_key_path`
- `cldr_tls_key_path_plaintext`
- `cldr_tls_key_password_file`
- `cldr_tls_csr_path`
- `cldr_tls_keystore_path`
- `cldr_tls_jdk_java_cacerts_search_paths`
- `cldr_tls_jdk_java_cacerts_location`
- `cldr_tls_jdk_java_cacerts_password `

Layer flags
- `cldr_tls_skip_cacerts_import` (default false, skips the generation of the uber truststore)

Layer roles:
- `fetch_ca`
- `sign_csr`
- `generate_csr`
- `generate_keystores`
- `apply_acls`
- `teardown`

Required provider roles:
- `setup_infra`
- `tls_common`
- `tls_fetch_ca`
- `tls_sign_csr`
- `tls_teardown`

Provider `tls_common` expected to populate:
- `cldr_tls_provider_ca_certificates`
