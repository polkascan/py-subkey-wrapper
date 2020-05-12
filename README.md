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
