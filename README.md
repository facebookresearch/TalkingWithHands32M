# Talking With Hands 16.2M 

This repository contains the data released in the ICCV 2019 paper, *Talking With Hands 16.2M: A Large-Scale Dataset of Synchronized Body-Finger Motion and Audio for Conversational Motion Analysis and Synthesis* . [pdf](http://openaccess.thecvf.com/content_ICCV_2019/papers/Lee_Talking_With_Hands_16.2M_A_Large-Scale_Dataset_of_Synchronized_Body-Finger_ICCV_2019_paper.pdf), [supplementary](http://openaccess.thecvf.com/content_ICCV_2019/supplemental/Lee_Talking_With_Hands_ICCV_2019_supplemental.pdf).



## Release 

This release contains majority of the entire dataset described in our paper: the motion data of 32 sessions. Each session contains several conversation tasks between a pair of persons, as described in our paper. In total, this release contains 116 takes, approximately 20 hours of conversation data. We are working to release other parts of the dataset in the future, including the audio.

**[NEW: 02/24/2021]** Now audio data of 17 sessions are released. Note we masked out (by setting audio sample values to 0) any audio segment that may relate to privacy or person identifiable information. The audio data of remaining sessions are under review & cleaning process now. Note only conversational takes have audios. The body gesture takes do not have audio.


### Unzip

If you cloned the whole repository, you can use the following command ([stackoverflow](https://stackoverflow.com/questions/107995/how-do-you-recursively-unzip-archives-in-a-directory-and-its-subdirectories-from)) to unzip the data.

```bash
cd mocap_data
find . -name "*.zip" | xargs -P 5 -I fileName sh -c 'unzip -o -d "$(dirname "fileName")/$(basename -s .zip "fileName")" "fileName"'
```



### Conversation takes

The dataset includes motion capture takes other than conversations, such as range of motion. We plan to provide additional information in the near future.

If you would like to use just the conversation takes, see `configs/conversations.json` to find out which takes are the conversation takes, and their corresponding lengths.

### Types of participants
There are two types of participants, _deep_ and _shallow_. Deep participants have participated across multiple sessions, while shallow participants had only one session. 

### Missing Data
We identified the following takes missing data for the shallow participant. We are working to address this issue. In the meantime,  you can still use the data of the deep participants for these takes.

session16/take7  session16/take8  session21/take12  session22/take16  session22/take17  

session22/take5 session22/take6  session22/take7  session24/take7  session28/take10

session28/take11 session28/take14  session28/take15  session28/take4  session28/take5


## Questions

If you have any specific questions regarding the released data, please email [Gilwoo Lee](mailto:gilwoo301@gmail.com).

## License
The TalkingWithHands dataset is CC-BY-NC 4.0 licensed, as found in the LICENSE file.

