# Build AlphaDroid for OnePlus Ace 3

## Prerequisites
- refer to [AOSP](https://source.android.com/docs/setup/start/requirements)

## Build
1. Initialise repo with [AlphaDroid](https://github.com/AlphaDroid-Project/manifest/tree/alpha-17.0) source code.
    ```
    repo init -u https://github.com/alphadroid-project/manifest.git -b alpha-17.0 --git-lfs
    ```

2. Download [aston manifest](https://github.com/AlphaDroid-devices/astonc-manifest/blob/alpha-17.0/local_manifest.xml) by cloning this repo
    ```
    git clone https://github.com/alphadroid-devices/astonc-manifest -b alpha-17.0 .repo/local_manifests
    ```

3. Sync
    ```
    repo sync 
    ```

4. Cook some bacon
    ```
    . build/envsetup.sh
    lunch alpha_<device>-[<release>]-user
    make bacon
    ```

    Or the light menu (no bacon)
    ```
    . build/envsetup.sh
    brunch aston
    ```
Enjoy! :)
