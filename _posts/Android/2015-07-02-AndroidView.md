---
layout: post
title: Android移动View
categories: Android
---

	    type A struct{}

			func main(){
				fmt.Println("asdasd")
			}

			func (a A)Say(i int32) *A{
				return &A{}
			}



	View CreateLayout(Context c,View cv)
	{
		RelativeLayout relativeLayout = new RelativeLayout(c);
		ViewGroup.LayoutParams lp = new ViewGroup.MarginLayoutParams(ViewGroup.LayoutParams.MATCH_PARENT, ViewGroup.LayoutParams.MATCH_PARENT);
		relativeLayout.setLayoutParams(lp);
		relativeLayout.addView(cv);
		//ChangeHeight(cv,360);
		return relativeLayout;
	}

	void ChangeHeight(View cv,int offset)
	{
		RelativeLayout.LayoutParams rp =(RelativeLayout.LayoutParams)cv.getLayoutParams();
		rp.bottomMargin = offset;
		rp.topMargin = -offset;
		cv.setLayoutParams(rp);
	}
