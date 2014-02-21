The *Booking* sample demonstrates a [synchronization](http://docs.aws.amazon.com/amazonswf/latest/awsrbflowguide/programming-workflow-patterns.html#programming-workflow-patterns-synchronization) workflow pattern. It waits for two activities to complete: a car reservation and airline reservation. When both activities complete, it sends a confirmation. All activities are performed asynchronously.

Prerequisites
=============

This sample requires the *AWS Flow Framework for Ruby*, which can be obtained and installed using the information here:

-   [https://aws.amazon.com/swf/flow/](https://aws.amazon.com/swf/flow/)

If you already have [Ruby](https://www.ruby-lang.org/) and [RubyGems](http://rubygems.org/) installed, you can install the framework by opening a terminal window and typing:

~~~~ {.literal-block}
gem install aws-flow
~~~~

For more information about setting up the AWS Flow Framework for Ruby, see [Installing the AWS Flow Framework for Ruby](http://docs.aws.amazon.com/amazonswf/latest/awsrbflowguide/installing.html) in the *AWS Flow Framework for Ruby Developer Guide*.

Download the Sample
===================

Download the sample by clicking the following link:

-   [Booking Sample](https://awsdocs.s3.amazonaws.com/swf/1.0/samples/Booking.zip)

Once you've downloaded the sample `.zip`, unarchive it and make note of the location you've expanded the archive into.

Run the Sample
==============

**To run the Booking sample:**

1.  Open a terminal window and change to the `lib` directory in the location where you unarchived the sample code. For example:

    ~~~~ {.literal-block}
    cd ~/Downloads/Booking/lib
    ~~~~

1.  Create a file in the `lib` directory called `credentials.cfg` and enter the following text, replacing the strings "insert ... access key here" with your AWS Access Key ID and your Secret Access Key.:

    ~~~~ {.literal-block}
    ---
    :access_key_id: "insert access key here"
    :secret_access_key: "insert secret access key here"
    ~~~~

2.  Execute the following commands on your command-line:

    ~~~~ {.literal-block}
    ruby booking_activity.rb &
    ruby booking_workflow.rb &
    ruby booking_workflow_starter.rb
    ~~~~

    Alternately, you can execute the run\_booking.sh shell script to run all of these commands at once.

For More Information
====================

For more information about the Amazon Simple Workflow service and the Amazon Flow Framework for Ruby, consult the following resources:

-   [AWS Flow Framework for Ruby Developer Guide](http://docs.aws.amazon.com/amazonswf/latest/awsrbflowguide/)
-   [AWS Flow Framework for Ruby API Reference](https://docs.aws.amazon.com/amazonswf/latest/awsrbflowapi/)
-   [AWS Flow Framework](http://aws.amazon.com/swf/flow/)
-   [Amazon Simple Workflow Service](http://aws.amazon.com/swf/)
