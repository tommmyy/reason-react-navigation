---
id: components/TouchableNativeFeedback
title: TouchableNativeFeedback
wip: true
---

```reason
type element;
type ref = React.Ref.t(Js.nullable(element));

module Background = {
  type t;

  [@bs.module "react-native"] [@bs.scope "TouchableNativeFeedback"]
  external selectableBackground: unit => t = "SelectableBackground";

  [@bs.module "react-native"] [@bs.scope "TouchableNativeFeedback"]
  external selectableBackgroundBorderless: unit => t =
    "SelectableBackgroundBorderless";

  [@bs.module "react-native"] [@bs.scope "TouchableNativeFeedback"]
  external canUseNativeForeground: unit => t = "CanUseNativeForeground";

  [@bs.module "react-native"] [@bs.scope "TouchableNativeFeedback"]
  external ripple: (string, bool) => t = "Ripple";
};

[@react.component] [@bs.module "react-native"]
external make:
  (
    ~ref: ref=?,
    // TouchableNativeFeedback props
    ~accessible: bool=?,
    ~accessibilityLabel: string=?,
    ~accessibilityComponentType: [@bs.string] [
                                   | `none
                                   | `button
                                   | `radiobutton_checked
                                   | `radiobutton_unchecked
                                 ]
                                   =?,
    ~accessibilityTraits: array(string)=?,
    ~delayLongPress: int=?,
    ~delayPressIn: int=?,
    ~delayPressOut: int=?,
    ~disabled: bool=?,
    ~hitSlop: Types.edgeInsets=?,
    ~onLayout: Event.layoutEvent => unit=?,
    ~onLongPress: Event.pressEvent => unit=?,
    ~onPress: Event.pressEvent => unit=?,
    ~onPressIn: Event.pressEvent => unit=?,
    ~onPressOut: Event.pressEvent => unit=?,
    ~pressRetentionOffset: Types.edgeInsets=?,
    ~style: Style.t=?,
    ~background: Background.t=?,
    ~useForeground: bool=?,
    ~testID: string=?,
    ~children: React.element
  ) =>
  React.element =
  "TouchableNativeFeedback";

```