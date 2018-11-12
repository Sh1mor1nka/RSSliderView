# RSSliderView
RSSliderView is a simple control for IOS based on UIView Class.

Here a preview:

![A preview of this control](http://i.piccy.info/i9/afdcd8b5029e1f28b8bd33f7bd3822c1/1424118139/12622/780425/123.png)

To create slider just do:

``` Objective-C
RSSliderView *horSlider = [[RSSliderView alloc] initWithFrame:CGRectMake(40, 40, 300, 80) andOrientation:Horizontal];
horSlider.delegate = self;
[horSlider setColorsForBackground:[UIColor colorWithRed:27.0/255.0 green:28.0/255.0 blue:37.0/255.0 alpha:1.0]
                       foreground:[UIColor colorWithRed:0.0 green:106.0/255.0 blue:95.0/255.0 alpha:1.0]
                           handle:[UIColor colorWithRed:0.0 green:205.0/255.0 blue:184.0/255.0 alpha:1.0]
                           border:[UIColor colorWithRed:0.0 green:205.0/255.0 blue:184.0/255.0 alpha:1.0]];
horSlider.label.text = @"Horizontal slider";
horSlider.label.font = [UIFont fontWithName:@"Helvetica" size:25];
horSlider.label.textColor = [UIColor colorWithRed:0.0 green:205.0/255.0 blue:184.0/255.0 alpha:1.0];
[self.view addSubview:horSlider];
```

after you set delegate you can get values from slider
``` Objective-C
-(void)sliderValueChanged:(RSSliderView *)sender {
    NSLog(@"Value Changed: %f", sender.value);
}

-(void)sliderValueChangeEnded:(RSSliderView *)sender {
    NSLog(@"Touch ended: %f", sender.value);
}
```
If you don't need handle
``` Objective-C
    [mySlider hideHandle];
```
If you don't like round corners or border
``` Objective-C
	[mySlider removeRoundCorners:YES removeBorder:YES];
```

## License

RSSliderView is licensed under the terms of the MIT license. Please see the [LICENSE](LICENSE) file for full details.
