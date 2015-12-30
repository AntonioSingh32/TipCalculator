#Pre-work - TipsCalculator

# TipsCalculator
Tip Calculator Application for Code Path Pre Work

//
//  ViewController.swift
//  TipCalculator
//
//  Created by Clark Kent on 12/27/15.
//  Copyright © 2015 Antonio Singh. All rights reserved.
//

import UIKit

class ViewController: UIViewController {

    @IBOutlet weak var billField: UITextField!
    @IBOutlet weak var tipLabel: UILabel!
    @IBOutlet weak var totalLabel: UILabel!
    @IBOutlet weak var tipField: UITextField!
    override func viewDidLoad() {
        super.viewDidLoad()
        // Do any additional setup after loading the view, typically from a nib.
        tipLabel.text = "$0.00"
        totalLabel.text = "$0.00"
    }

    override func didReceiveMemoryWarning() {
        super.didReceiveMemoryWarning()
        // Dispose of any resources that can be recreated.
    }

    @IBAction func onEditingChanged(sender: AnyObject) {
    
    let billAmount = NSString (string: billField.text!).doubleValue
    let percent = NSString (string: tipField.text!).doubleValue
    let tip = billAmount * percent/100
    let total = billAmount + tip
    
        
    tipLabel.text = "$\(tip)"
    totalLabel.text = "$\(total)"
        
    tipLabel.text = String (format: "$%.2f", tip)
    totalLabel.text = String (format: "$%.2f", total)
        
    }

    @IBAction func onTap(sender: AnyObject) {
    view.endEditing(true)

    }
}

Tips Calculator is a tip calculator application for iOS.

Submitted by: Antonio Singh

Time spent: 7 hours spent in total


![My image](https://fat.gfycat.com/YellowishHandyAmericanavocet.gif)

#User Stories

* [ ] User can enter a bill amount, choose a tip percentage, and see the tip and total values.

## Video Walkthrough

<img src='https://fat.gfycat.com/YellowishHandyAmericanavocet.gif' title='Video Walkthrough' width='' alt='Video Walkthrough' />
