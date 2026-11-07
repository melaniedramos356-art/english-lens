# 验证记录

- 2026-11-07：assembleDebug、testDebugUnitTest、lintDebug 全部通过。
- 框选坐标测试 5 项，失败 0；lint 无错误，仍有依赖更新和中文文本国际化提示。
- apksigner 验证通过：APK v2 签名，Android Debug 测试证书。
- APK 权限核对：INTERNET、ACCESS_NETWORK_STATE 与应用内部 receiver 权限，无通讯录、定位、麦克风、全部相册访问权限。
- 已验证 MyMemory 实际 HTTPS 请求：`She leaves home at seven.` 返回中文参考翻译。
- 已验证词典包含 leaves、went 等变形索引，保留原形歧义。
- 未验证：小米14安装、拍照权限交互、实际 OCR 精度、手机英语 TTS、屏幕排版及大陆手机网络。

真机验收：安装 → 拍摄清晰英文 → 框选并识别 → 修改文字 → 生成可点击单词 → 点词查看卡片 → 朗读/停止/慢速 → 确认联网并翻译 → 撤回授权 → 再次翻译重新询问。
另测：拒绝联网、无网络、长句超过500字节、空图片、竖拍横拍、取消拍照、缺失英语语音。任何崩溃或错误翻译都应记录后修复。
