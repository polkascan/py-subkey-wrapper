# py-subkey
Python wrapper for Parity Subkey: https://github.com/paritytech/substrate/tree/master/bin/utils/subkey

## Examples

### Using local binary
```python
sub_key = Subkey(subkey_path='/usr/local/bin/subkey')
print(sub_key.generate_key(network='kusama'))
```

### using Docker machine with default image parity/subkey:latest
```python
sub_key = Subkey(use_docker=True)
print(sub_key.generate_key(network='kusama'))
```

### Using Docker machine with alternate image
```python
sub_key = Subkey(use_docker=True, docker_image='polkasource/subkey:v2.0.0-alpha.3')
print(sub_key.generate_key(network='kusama'))
```

### Inspect a suri (example with derivation path)
```python
sub_key = Subkey(use_docker=True)
subkey_result = sub_key.inspect(network='kusama', suri="appear fortune produce assist volcano deal shoulder foot engine harvest pupil agent//Alice")
```
