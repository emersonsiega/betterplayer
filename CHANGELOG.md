## 0.0.45
* Added Picture in Picture support.
* Added new parameters in BetterPlayerControlsConfiguration: pipMenuIcon and enablePip.
* Added new methods in BetterPlayerController: enablePictureInPicture, disablePictureInPicture, isPictureInPictureSupported,
setBetterPlayerGlobalKey.
* Added Picture in Picture icon in player controls.
* Added Picture in Picture example.
* Updated ExoPlayer version.
* Added pipStart and pipStop events.
* [BREAKING_CHANGE] Removed skipsTimeInMilliseconds. Added forwardSkipTimeInMilliseconds and backwardSkipTimeInMilliseconds.
* Updated notification service in android example.
* Fixed event play/pause event not triggered when controlling video with PiP or remote notification.
* Fixed playerTheme not set correctly.
* Fixed progress bar able to drag over other buttons.
* Fixed iOS player last second issue (player did not complete on last second of resource).

## 0.0.44
* Added placeholder until play example
* Added playback stalled feature in iOS. iOS version should behave same as Android once video failed to load.
* Added BetterPlayerTheme to controls configuration (added by https://github.com/maine98).
* [BREAKING_CHANGE] Changed custom controls builder in BetterPlayerControlsConfiguration. Now it accepts BetterPlayerController.
* Exposed BetterPlayerPlaylistState and betterPlayerController getter within.
* Added overriddenDuration to BetterPlayerDataSource.

## 0.0.43
* Added autoDispose flag in BetterPlayerConfiguration
* Added removeEventsListener in BetterPlayerController
* Video list examples update
* Fixed Android native build warnings
* Fixed placeholder until play issues
* Added placeholderOnTop to the BetterPlayerConfiguration
* Lint fixes

## 0.0.42
* Fixed resolution issue
* Fixed type of BetterPlayerDataSource for file type
* Added audio notify on dispose (iOS) (fixed by https://github.com/kingiol)

## 0.0.41
* Fixed loadingColor and loadingWidget for cupertino player
* Increased size of cupertino buttons
* Fixed setControlsEnabled in cupertino/material player
* [BREAKING_CHANGE] Removed startAt, looping, placeholder, overlay, fullScreenByDefault,
 allowedScreenSleep, systemOverlaysAfterFullScreen, deviceOrientationsAfterFullScreen from BetterPlayerController

## 0.0.40
* Exposed VideoPlayerValue in export
* Fixed log issue
* Added loadingColor and loadingWidget in BetterPlayerControlsConfiguration

## 0.0.39
* Added lint library for dart analysis
* [BREAKING_CHANGE] Changed constant names to lowerCamelCase in BetterPlayerDataSourceType
* [BREAKING_CHANGE] Changed constant names to lowerCamelCase in BetterPlayerEventType
* [BREAKING_CHANGE] Changed constant names to lowerCamelCase in BetterPlayerSubtitlesSourceType

## 0.0.38
* Added support for player notifications
* Added handleLifecycle to BetterPlayerConfiguration
* Added notificationConfiguration to BetterPlayerDataSource

## 0.0.37
* Added setControlsEnabled to BetterPlayerController
* Fixed example video list widget buttons not rendering correctly in small resolutions
* Added setOverriddenAspectRatio to BetterPlayerController
* Fixed crash connected with setSpeed in Android platform
* Fixed deviceOrientationsOnFullScreen for iOS
* Fixed CH translations (fixes by https://github.com/JarvanMo)
* Click to show/hide controls (fixed by https://github.com/mtAlves)
* [BREAKING_CHANGE] Removed future from isPlaying. Now it's sync method (https://github.com/hongfeiyang)

## 0.0.36
* Added INITIALIZED event
* Added autoDetectFullscreenDeviceOrientation in BetterPlayerConfiguration
* Fixed autoPlay background issue
* Removed open_iconic_flutter icons used in Cupertino controls
* Added cupertino_icons for icons used Cupertiono controls
* Fixed progress bar not working correctly for iOS 12 with file datasource
* Removed yellow line below progress text (fixed by https://github.com/mtAlves)

## 0.0.35
* Fixed iOS black screen issue
* Fixed full screen placeholder issue
* Fixed event not firing in enterFullScreen and exitFullScreen
* Fixed subtitles parsing issues

## 0.0.34
* Added memory data source
* Added factories: network, file, memory for BetterPlayerDataSource
* Fixed missing useHlsTracks implementation
* Fixed placeholder showing after full screen when using showPlaceholderUntilPlay
* Added setControlsVisibility to BetterPlayerController
* [BREAKING_CHANGE] Removed showControlsOnInitialize from BetterPlayerConfiguration. Use BetterPlayerControlsConfiguration to set showControlsOnInitialize parameter.
* Fixed cupertino controls issue with hasError

## 0.0.33
* Fixed BetterPlayerEvent visibility
* Fixed lazy initialization, when first data source is passed after player finishes first render
* Added selectedByDefault to BetterPlayerSubtitlesConfiguration
* Fixed HLS tracks android native code
* Updated example

## 0.0.32
* Fixed locale picking when context is not mounted anymore
* Added cache feature (based on https://github.com/sanekyy/plugins/tree/caching and https://github.com/vikram25897/flutter_cached_video_player solutions)
* Added BetterPlayerCacheConfiguration to BetterPlayerDataSource
* Refactored Android's native code

## 0.0.31
* Added showPlaceholderUntilPlay in BetterPlayerConfiguration
* Fixed exception event not being triggered
* Fixed controls not displaying on video finished

## 0.0.30
* Fixed issue when full screen was triggered twice if autoPlay and fullScreenByDefault were enabled
* Removed flutter_widgets, since it's not maintained anymore. Added instead visibility_detector package (by https://github.com/espresso3389)
* Added rewind and forward buttons for android player.
* Fixed player UI's jank
* Added enableSkips and skipsTimeInMilliseconds in BetterPlayerControlsConfiguration
* Changed middle play button behavior (now it's only used for restart player).
* Updated BetterPlayerControllerProvider visibility.
* Override invalid dependency from wakelock library.

## 0.0.29+1
* Updated readme

## 0.0.29
* Fixed routePageBuilder usage from BetterPlayerConfiguration
* Added overflowMenuIcon, playbackSpeedIcon, qualitiesIcon, subtitlesIcon, overflowMenuIconsColor to BetterPlayerControlsConfiguration
* Added double tap to play/pause video (original idea by https://github.com/r6c)

## 0.0.28
* Fixed subtitles overflow issue when transitioning between fullscreen and normal state
* Added alignment and backgroundColor in BetterPlayerSubtitlesConfiguration

## 0.0.27
* Added enableOverflowMenu option in BetterPlayerControlsConfiguration (enable/disable overflow menu)
* Added overflowMenuCustomItems in BetterPlayerControlsConfiguration (show custom menu items in overflow menu)
* [BREAKING_CHANGE] Removed defaultErrorText, loadingNextVideoText, liveText from BetterPlayerControlsConfiguration. To change these values, please use translations in BetterPlayerConfiguration.
* Added BetterPlayerTranslations in BetterPlayerConfiguration. You can use it to setup translations of the player.

## 0.0.26
* Added fullScreenAspectRatio and deviceOrientationsOnFullScreen to handle different full screen scenarios
* Updated wakelock version

## 0.0.25
* [BREAKING_CHANGE]: changed API in BetterPlayerControlsConfiguration: enableQualities replaces enableTracks.
* Added support for different video resolutions
* Fixed issue when full screen is being dismissed on changing subtitles
* Added CHANGED_RESOLUTION event

## 0.0.24
* Added possibility to set multiple subtitles to video
* [BREAKING_CHANGE]: changed API in BetterPlayerDataSource. Instead of one subtitles object, list of subtitles is required.

## 0.0.23
* General bug fixes.
* Added playerVisibilityChangedBehavior in BetterPlayerConfiguration.
* Changed player behavior when player is not visible in viewport: if player was playing before leaving viewport it will be paused and if user views player again it will start playing automatically.
* Added BetterPlayer.network and BetterPlayer.file methods.
* Changed iOS & Android native classes name to prevent conflict issues with video_player.

## 0.0.22
* Added support for hls tracks (quality of the videos).
* Added useHlsTracks and hlsTrackName in BetterPlayerDataSource.
* Added CHANGED_TRACK event.
* You can choose track from overflow menu. When there's no tracks to select "Default" will be selected.

## 0.0.21
* Added enableSubtitles parameter.

## 0.0.20
* Added rotation parameter in BetterPlayerConfiguration.

## 0.0.19
* Added support for hls subtitles (BetterPlayer will handle them automatically).
* [BREAKING_CHANGE]: changed API in BetterPlayerSubtitlesSource. To use old API, please use factory: BetterPlayerSubtitlesSource.single.
* Added useHlsSubtitles parameter in BetterPlayerDataSource.
* Added CHANGED_SUBTITLES event.
* User can choose subtitles from overflow menu, when there's no subtitles selected, "none" options will be chosen.

## 0.0.18:
* Fixed loading issue when auto play video feature is enabled in playlist.

## 0.0.17
* Fixed placeholder not following video fit options (fixed by https://github.com/nicholascioli).
* Updated dependencies.

## 0.0.16
* Added overflow menu.
* Added playback speed feature (based on https://github.com/shiyiya solution).
* User can choose playback speed from overflow menu.
* Added SET_SPEED event.

## 0.0.15
* Added fit configuration option (based on https://github.com/shiyiya solution).

## 0.0.14
* Better player list video player state is preserved on state changed.
* Fixed manual dispose issue.
* Fixed playlists video changing issue (fixed by https://github.com/sokolovstas).
* Added tap to hide feature for iOS player (by https://github.com/gazialankus).
* Fixed CONTROLS_VISIBLE and CONTROLS_HIDDEN events not triggered for ios player (fixed by https://github.com/gazialankus).
* Added seek method to BetterPlayerListVideoPlayerController.

## 0.0.13
* Changed channel name of video player plugin.
* Fixed dispose issue in cupertino player.

## 0.0.12
* Fixed duration called on null (fixed by https://github.com/ganeshrvel).
* Added new control events (fixed by https://github.com/ganeshrvel).
* Fixed .m3u8 live stream issues in iOS.

## 0.0.11
* Fixed iOS crash on dispose.
* Added player headers support.
* Updated dependencies.
* Dart Analysis refactor.

## 0.0.10
* Added BetterPlayerListVideoPlayerController to control list video player.

## 0.0.9
* Fixed setState called after dispose.
* General bugfixes.

## 0.0.8
* Fixed buffering indicator issue on Android.

## 0.0.7
* Fixed progress bar scroll lag.

## 0.0.6
* Fixed video duration issue.
* Added HTML subtitles.

## 0.0.5
* Added reusable video player.
* Bug fixes.

## 0.0.4
* Changed 'settings' to 'configuration'.
* Removed unused parameters from configuration.
* Documentation update.

## 0.0.3
* Updated documentation.

## 0.0.2
* Moved example project from better_player_example to example.

## 0.0.1
* Initial release.
