# glTF-Transform-lod-script

This is a script to make LODs for an [glTF](https://registry.khronos.org/glTF/specs/2.0/glTF-2.0.html) asset with [`glTF-Transform`](https://gltf-transform.donmccurdy.com/).

This script is based on [this example script](https://gist.github.com/donmccurdy/2226332bb58980caebcd21fe7cbca029).

LODs are defined with [glTF `MSFT_lod` extension](https://github.com/KhronosGroup/glTF/blob/main/extensions/2.0/Vendor/MSFT_lod/README.md).

## How to use

```
# Clone this repository
$ git clone https://github.com/takahirox/glTF-Transform-lod-script
$ cd glTF-Transform-lod-script

# Install dependencies
$ npm install @gltf-transform/core @gltf-transform/functions meshoptimizer command-line-args

# Run
$ node generate_lod.mjs in.glb out.glb \
 --ratio 0.5,0.1 \
 --error 0.01,0.05 \
 --coverage 0.7,0.3,0.0 \
 --texture 512x512,128x128
```

## Options


| Option | Description | Example | Required |
| ------ | ----------- | ------- | -------- |
| `--ratio ratio_values` | T.B.D. | `--ratio 0.5,0.1` | Yes |
| `--error error_values` | T.B.D. | `--error 0.01,0.05` | Yes |
| `--coverage coverage_values` | T.B.D. | `--coverage 0.7,0.3,0.0` | Yes |
| `--texture texture_values` | T.B.D. | `--texture 512x512,128x128` | Yes |
| `--interleaved` | T.B.D. | `--interleaved` | No |


## Limitations

This script is not guaranteed to work for all the glTF assets especially if they are complex or have extensions. Please edit the script on your end if it doesn't work for your assets.
