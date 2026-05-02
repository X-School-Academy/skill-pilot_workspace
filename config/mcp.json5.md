Env placeholder rules used in this file:
 - `${VAR}`: required. The MCP loader marks the server as missing env when VAR is unset.
 - `${VAR:-}`: optional. Missing VAR resolves to an empty string.
 - `${VAR:-default}`: optional with fallback. Missing VAR resolves to `default`.
 - `${VAR-default}`: fallback only when VAR is unset; an explicit empty value is preserved.
