# Useful commands
> note: already define /bin path for elasticsearch

## Reset password elastic
`$ elasticsearch-reset-password -u elastic`

## create enrollment token
`elasticsearch-create-enrollment-token -s node`
`elasticsearch-create-enrollment-token -s kibana --url "https://172.0.0.3:9200"`
