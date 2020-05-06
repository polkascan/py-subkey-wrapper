# py-subkey
Python subkey wrapper

## Examples

### Using local binary
```python
sub_key = Subkey(subkey_path='/usr/local/bin/subkey')
print(sub_key.generate_key(network='kusama'))
```

### Using docker machine
```python
sub_key = Subkey(use_docker=True)
print(sub_key.generate_key(network='kusama'))
```

### Using docker machine with alternate image
```python
sub_key = Subkey(use_docker=True, docker_image='polkasource/subkey:v2.0.0-alpha.3')
print(sub_key.generate_key(network='kusama'))
```

### Create signature with subkey
```python

account_key = "polar original upset crater jazz among universe brain rack choice below spice"

# Create signature payload
signature_payload = ScaleDecoder.get_decoder_class('ExtrinsicPayloadValue')

signature_payload.encode({
    'call': str(call.data),
    'era': era,
    'nonce': nonce,
    'tip': tip,
    'specVersion': self.runtime_version,
    'genesisHash': genesis_hash,
    'blockHash': genesis_hash
})

# Sign payload
signature = sub_key.sign(str(signature_payload.data), account_key)
```
