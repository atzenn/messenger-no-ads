# Messenger No Ads

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](./LICENSE)

The best free & open source tweak for Messenger  
Not only removing ads but shipped with many nice features

<img src="https://haoict.github.io/cydia/images/newmessengernoads.jpg" alt="Messenger No Ads" width="414"/>

## Features

- No Ads
- Disable Read Receipt. Can be added to Control center for quickly turn on/off. *Go to Setting -> Control Center -> Customize Controls -> Add Messenger No Ads*
- Disable Typing Indicator
- Disable Story Seen (see others's stories but they won't know it)
- Can save friend's story. (Tap ... on top right of story view -> Save)
- Hide Search Bar (iOS12) / Hide Stories Row / Hide People tab
- Support iOS 11 (tested) - 12 (tested) - 13 (tested)
- Support latest Messenger version (If it doesn't work, you should update the app to latest version 258.0 - 260.1)

## Cydia Repo

[https://haoict.github.io/cydia](https://haoict.github.io/cydia)

## Building

[Theos](https://github.com/theos/theos) required.

```bash
make do
```

## Contributors

Thank you to my friends all around the world who helped me on translation:  
- mahmoud ahmad  
- Complex Assassin  
- Michael Basquill  
- BenCoro  
- TC@BE  

Contributions of any kind welcome!

## License

Licensed under the MIT License, Copyright © 2020-present Hao Nguyen <hao.ict56@gmail.com>

## [Note] Advanced thingy for development
<details>
  <summary>Click to expand!</summary>
  
  Add your device IP in `~/.bash_profile` or in project's `Makefile` for faster deployment
  ```base
  THEOS_DEVICE_IP = 192.168.1.21
  ```

  Add SSH key for target deploy device so you don't have to enter ssh root password every time
  ```bash
  cat ~/.ssh/id_rsa.pub | ssh -p 22 root@192.168.1.21 "mkdir -p ~/.ssh && cat >> ~/.ssh/authorized_keys"
  ```

  Build the final package
  ```bash
  FINALPACKAGE=1 make package
  ```

</details>