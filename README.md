module two_bit_magnitudecom(
input a0,
input a1,
input b0,
input b1,
output p,
output r,
output q,
);
assign q=((~a1)^(b1))&(a0&b0);
assign p=((~a1)&(b1))|(b0&(~a0)&(~a1))|((a0)&b1&b0));
assign r=((a1&(~b1))|((~b0)&a1&a0)|(a0&(b1)&(~b0)));
