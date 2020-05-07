# Talking With Hands 16.2M 

This repository contains the data released in the ICCV 2019 paper, *Talking With Hands 16.2M: A Large-Scale Dataset of Synchronized Body-Finger Motion and Audio for Conversational Motion Analysis and Synthesis* . [pdf](http://openaccess.thecvf.com/content_ICCV_2019/papers/Lee_Talking_With_Hands_16.2M_A_Large-Scale_Dataset_of_Synchronized_Body-Finger_ICCV_2019_paper.pdf), [supplementary](http://openaccess.thecvf.com/content_ICCV_2019/supplemental/Lee_Talking_With_Hands_ICCV_2019_supplemental.pdf).



## Release 

This release contains majority of the entire dataset described in our paper: the motion data of 32 sessions. Each session contains several conversation tasks between a pair of persons, as described in our paper. In total, this release contains 116 takes, approximately 20 hours of conversation data. We are working to release other parts of the dataset in the future, including the audio.



### Unzip

If you cloned the whole repository, you can use the following command ([stackoverflow](https://stackoverflow.com/questions/107995/how-do-you-recursively-unzip-archives-in-a-directory-and-its-subdirectories-from)) to unzip the data.

```bash
cd mocap_data
find . -name "*.zip" | xargs -P 5 -I fileName sh -c 'unzip -o -d "$(dirname "fileName")/$(basename -s .zip "fileName")" "fileName"'
```



### Conversation takes

The dataset includes motion capture takes other than conversations, such as range of motion. We plan to provide additional information in the near future.

If you would like to use just the conversation takes, see `configs/conversations.json` to find out which takes are the conversation takes, and their corresponding lengths.



## Questions

If you have any specific questions regarding the released data, please email [Gilwoo Lee](mailto:gilwoo301@gmail.com).

## License
The TalkingWithHands dataset is CC-BY-NC 4.0 licensed, as found in the LICENSE file.

